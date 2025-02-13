### Example 1: Using the Invoke-MgBetaReplyGroupThread Cmdlet
```powershell
Import-Module Microsoft.Graph.Beta.Groups
$params = @{
	Post = @{
		Body = @{
			ContentType = ""
			Content = "content-value"
		}
	}
}
Invoke-MgBetaReplyGroupThread -GroupId $groupId -ConversationThreadId $conversationThreadId -BodyParameter $params
```
This example shows how to use the Invoke-MgBetaReplyGroupThread Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).
### Example 2: Using the Invoke-MgBetaReplyGroupThread Cmdlet
```powershell
Import-Module Microsoft.Graph.Beta.Groups
$params = @{
	Post = @{
		Body = @{
			ContentType = "text"
			Content = "Which quarter does that file cover? See my attachment."
		}
		Attachments = @(
			@{
				"@odata.type" = "#microsoft.graph.fileAttachment"
				Name = "Another file as attachment"
				ContentBytes = "VGhpcyBpcyBhIGZpbGUgdG8gYmUgYXR0YWNoZWQu"
			}
		)
	}
}
Invoke-MgBetaReplyGroupThread -GroupId $groupId -ConversationThreadId $conversationThreadId -BodyParameter $params
```
This example shows how to use the Invoke-MgBetaReplyGroupThread Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).
### Example 3: Using the Invoke-MgBetaReplyGroupThread Cmdlet
```powershell
Import-Module Microsoft.Graph.Beta.Groups
$params = @{
	Post = @{
		Body = @{
			ContentType = "text"
			Content = "I attached an event."
		}
		Attachments = @(
			@{
				"@odata.type" = "#microsoft.graph.itemAttachment"
				Name = "Holiday event"
				Item = @{
					"@odata.type" = "microsoft.graph.event"
					Subject = "Discuss gifts for children"
				}
			}
		)
	}
}
Invoke-MgBetaReplyGroupThread -GroupId $groupId -ConversationThreadId $conversationThreadId -BodyParameter $params
```
This example shows how to use the Invoke-MgBetaReplyGroupThread Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).
### Example 4: Using the Invoke-MgBetaReplyGroupThread Cmdlet
```powershell
Import-Module Microsoft.Graph.Beta.Groups
$params = @{
	Post = @{
		Body = @{
			ContentType = "text"
			Content = "I attached a reference to a file on OneDrive."
		}
		Attachments = @(
			@{
				"@odata.type" = "#microsoft.graph.referenceAttachment"
				Name = "Personal pictures"
				SourceUrl = "https://contoso.com/personal/mario_contoso_net/Documents/Pics"
				ProviderType = "oneDriveConsumer"
				Permission = "Edit"
				IsFolder = "True"
			}
		)
	}
}
Invoke-MgBetaReplyGroupThread -GroupId $groupId -ConversationThreadId $conversationThreadId -BodyParameter $params
```
This example shows how to use the Invoke-MgBetaReplyGroupThread Cmdlet.
To learn about permissions for this resource, see the [permissions reference](/graph/permissions-reference).
