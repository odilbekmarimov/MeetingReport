# Data Dictionary (From Excel File)

## Table: `dim_comm_type`

| Column Name    | Description                                            |
| -------------- | ------------------------------------------------------ |
| `comm_type`    | Type of the communication (e.g., email, meeting, chat) |
| `comm_type_id` | Unique identifier for the communication type           |

## Table: `dim_subject`

| Column Name  | Description                             |
| ------------ | --------------------------------------- |
| `subject`    | Subject or topic of the communication   |
| `subject_id` | Unique identifier for the subject entry |

## Table: `dim_user`

| Column Name   | Description                    |
| ------------- | ------------------------------ |
| `user_id`     | Unique identifier for the user |
| `name`        | Full name of the user          |
| `email`       | Email address of the user      |
| `location`    | User's location (if available) |
| `displayName` | Name as shown in display or UI |
| `phoneNumber` | Contact number of the user     |

## Table: `dim_calendar`

| Column Name       | Description                            |
| ----------------- | -------------------------------------- |
| `raw_calendar_id` | Raw reference ID for the calendar data |
| `calendar_id`     | Unique identifier for calendar entry   |

## Table: `dim_audio`

| Column Name     | Description                            |
| --------------- | -------------------------------------- |
| `raw_audio_url` | URL or file path to the raw audio      |
| `audio_id`      | Unique identifier for the audio record |

## Table: `dim_video`

| Column Name     | Description                            |
| --------------- | -------------------------------------- |
| `raw_video_url` | URL or file path to the raw video      |
| `video_id`      | Unique identifier for the video record |

## Table: `dim_transcript`

| Column Name          | Description                             |
| -------------------- | --------------------------------------- |
| `raw_transcript_url` | URL pointing to the raw transcript file |
| `transcript_id`      | Unique identifier for the transcript    |

## Table: `fact_communication`

| Column Name     | Description                                                |
| --------------- | ---------------------------------------------------------- |
| `comm_id`       | Unique identifier for the communication                    |
| `raw_id`        | Reference to the raw communication content                 |
| `source_id`     | Original source identifier of the communication            |
| `comm_type_id`  | Communication type (linked to `dim_comm_type`)             |
| `subject_id`    | Subject identifier (linked to `dim_subject`)               |
| `calendar_id`   | Calendar identifier (linked to `dim_calendar`)             |
| `audio_id`      | Audio record identifier (linked to `dim_audio`)            |
| `video_id`      | Video record identifier (linked to `dim_video`)            |
| `transcript_id` | Transcript identifier (linked to `dim_transcript`)         |
| `datetime_id`   | DateTime reference for the communication                   |
| `ingested_at`   | Timestamp when the communication was ingested              |
| `processed_at`  | Timestamp when the communication was processed             |
| `is_processed`  | Boolean flag indicating if the communication was processed |
| `raw_title`     | Original title or subject from the raw data                |
| `raw_duration`  | Raw duration string or value as received                   |

## Table: `bridge_comm_user`

| Column Name     | Description                                          |
| --------------- | ---------------------------------------------------- |
| `comm_id`       | Reference to the communication ID                    |
| `user_id`       | Reference to the user ID                             |
| `isAttendee`    | Indicates if the user attended the communication     |
| `isParticipant` | Indicates if the user was listed as a participant    |
| `isSpeaker`     | Indicates if the user spoke during the communication |
| `isOrganiser`   | Indicates if the user was the organiser              |
