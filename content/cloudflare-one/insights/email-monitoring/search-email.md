---
title: Search email
pcx_content_type: how-to
weight: 2
---

# Search email

With Email Security, you can use different screen criteria to search through your email, reclassify and move a certain volume of messages, find similar emails, and export messages.

## Screen criteria

Email Security allows you to use popular, regular, and advanced screening criteria to search through your inbox. Advanced screening will give you the most in-depth investigation of your inbox.

To screen through your email traffic:

1. Log in to [Zero Trust](https://one.dash.cloudflare.com/).
2. Select **Email Security**.
3. Select **Investigation**, then **Run new screen**.
4. Choose between **Popular**, **Regular**, and **Advanced** screen methods. Refer to the explanation below to learn what each method does.

The results will be displayed on a table. The table allows you to review and take action on the messages that match your chosen screening criteria.

### Popular screen

A popular screen allows you to view messages based on common pre-defined criteria.

To use a popular screen criteria:

1. Under **Method**, select **Popular screens**.
2. Select one of the following criteria:
   * **Moved emails**: View emails automatically or manually moved within the last seven days.
   * **Reclassified emails**: Emails that had their disposition reclassified within the last seven days.
   * **Malicious emails**: Emails assigned the malicious disposition within the last seven days.
   * **Spoof emails**: Emails assigned the spoof disposition within the last seven days.
   * **Suspicious emails**: Emails assigned the suspicious disposition within the last seven days.
   * **Spam emails**: Emails assigned to the spam disposition within the last seven days.
3. Select **Run screen**.

To modify your screening criteria, under **Active screen criteria**, select **Modify**.

### Regular screen

A regular screen allows you to investigate your inbox by inserting a term to screen across all criteria.

To use a regular screen criteria:

1. Under **Method**, select **Regular screen**.
2. Select a **Date range**.
3. Enter a keyword.
4. Select **Run screen**.

To include all emails as part of the search, enable **Include all mail**.

To modify your screening criteria, under **Active screen criteria**, select **Modify**.

To reset your screening criteria, select **Reset**.

### Advanced screen

The advanced screen criteria gives you the option to narrow message results based on specific criteria. The advanced screen has several options (such as keywords, subject keywords, sender domain, and more) to scan your inbox.

To use advanced screen criteria:

1. Under **Method**, select **Advanced screen**.
2. (Required) Select a date range.
3. (Optional) Fill in the other fields. All fields, except for **Subject**, must be filled with one value only.
4. Select **Run screen**.

To include all emails as part of the search, enable **Include all mail**.

To modify your screening criteria, under **Active screen criteria**, select **Modify**.

To reset your screening criteria, select **Reset**.

## Reclassify messages

Reclassifying messages allows you to choose the disposition of your messages if the disposition is incorrect.

To reclassify a message:

1. On the **Investigation** page, under **Your matching messages**, select the message you want to reclassify.
2. Select the three dots, then select **Reclassify**. 
3. Under **New disposition**, select among the following:
   * **Malicious**: Traffic invoked multiple phishing verdict triggers, met thresholds for bad behavior, and is associated with active campaigns.
   * **Spoof**: Traffic associated with phishing campaigns that is either non-compliant with your email authentication policies (SPF, DKIM, DMARC) or has mismatching Envelope From and `Header From` values.
   * **Spam**: Traffic associated with non-malicious, commercial campaigns.
   * **Bulk**: Traffic associated with [Graymail](https://en.wikipedia.org/wiki/Graymail_%28email%29), that falls in between the definitions of `SPAM` and `SUSPICIOUS`. For example, a marketing email that intentionally obscures its unsubscribe link.
   * **Clean**: Traffic not associated with any phishing campaigns.
4. Select **Save**.

To reclassify messages in bulk, select the messages you want to reclassify > **Action** > **Reclassify**.

## Move messages

Moving messages allows you to move messages to a specific folder.

To move messages:

1. On the **Investigation** page, select all the messages you want to move.
2. Select the **Action** dropdown, then select **Move**.
3. Select among one of the following folders:
   * **Inbox**: Move messages to the primary email folder.
   * **Junk email**: Move messages to the junk or spam folder.
   * **Trash**: Move messages to the trash or deleted items email folder.
   * **Soft delete (user recoverable)**: Move messages to the user's Deleted Items folder. This option is for Microsoft O365 only.
   * **Hard delete (admin recoverable)**: Delete messages from a user's inbox.
4. Select **Save**.

## Find similar emails

Each detection has an Electronic Detection Fingerprint (EDF) hash that Email Security sends to the Search API to retrieve similar detections.

To find similar detection results:

1. On the **Investigation** page, under **Your matching messages**, search for the **Similar emails** column.
2. Select the number of similar emails. Selecting the number will show you a list of similar emails.

## Export messages

With Email Security, you can export messages to a CSV file.

To export messages:

1. On the **Investigation** page, under **Your matching messages**, select **Export to CSV**.
2. Select **Export messages** on the pop-up message. You can only export up to 1,000 rows from the dashboard.

## Email status

Email Security allows you to review the status and actions of each email.

To view status and actions for each email:

1. On the **Investigation** page, select the three dots.
2. Selecting the three dots will show you the following options:
   - If the email is quarantined: 
      - **View details**: Refer to [Email details](/cloudflare-one/roles-permissions/#email-details) to learn more.
      - **View similar emails**: Find similar emails based on the `value_edf_hash` (Electronic Detection Fingerprint hash).
      - **Release**: Email Security will no longer quarantine your chosen messages.
      - **Reclassify**: Choose the dispositions of your messages if they are incorrect. Refer to [Reclassify messages](/cloudflare-one/insights/email-monitoring/search-email/#reclassify-messages) to learn more.
3. If the email is not quarantined:
   - **View details**.
   - **View similar**.
   - [Move](/cloudflare-one/email-security/auto-moves/) (only available if you authorized moves).
   - **Reclassify**.