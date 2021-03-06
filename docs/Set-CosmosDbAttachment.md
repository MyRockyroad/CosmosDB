---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# Set-CosmosDbAttachment

## SYNOPSIS

Update am attachment for a Cosmos DB document.

## SYNTAX

### Context (Default)

```powershell
Set-CosmosDbAttachment -Context <Context> [-Database <String>] [-Key <SecureString>] -CollectionId <String>
 -DocumentId <String> -Id <String> [-NewId <String>] [-PartitionKey <String[]>] [-ContentType <String>]
 [-Media <String>] [-Slug <String>] [<CommonParameters>]
```

### Account

```powershell
Set-CosmosDbAttachment -Account <String> [-Database <String>] [-Key <SecureString>] [-KeyType <String>]
 -CollectionId <String> -DocumentId <String> -Id <String> [-NewId <String>] [-PartitionKey <String[]>]
 [-ContentType <String>] [-Media <String>] [-Slug <String>] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will update an existing attachment in a Cosmos DB
document.

## EXAMPLES

### Example 1

```powershell
PS C:\> Set-CosmosDbAttachment -Context $cosmosDbContext -CollectionId 'MyNewCollection' -DocumentId 'ac12345' -Id 'image_1' -NewId 'Image_2'
```

Rename the Id of an attachment for a document in a collection.

### Example 2

```powershell
PS C:\> Set-CosmosDbAttachment -Context $cosmosDbContext -CollectionId 'MyNewCollection' -DocumentId 'ac12345' -Id 'image_1' -NewId 'Image_2' -PartitionKey 'Id'
```

Rename the Id of an attachment for a document in a collection that
has a partition key.

## PARAMETERS

### -Account

The account name of the Cosmos DB to access.

```yaml
Type: String
Parameter Sets: Account
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

This is the Id of the collection to update the attachment for.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentType

Not Required to be set when attaching raw media.
This is a user settable property.
It notes the content type of the attachment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context

This is an object containing the context information of the Cosmos DB database
that will be deleted. It should be created by \`New-CosmosDbContext\`.

```yaml
Type: Context
Parameter Sets: Context
Aliases: Connection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

The name of the database to access in the Cosmos DB account.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DocumentId

This is the Id of the collection to update the attachment for.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This is the Id of the attachment to update.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Key

The key to be used to access this Cosmos DB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType

The type of key that will be used to access ths Cosmos DB.

```yaml
Type: String
Parameter Sets: Account
Aliases:
Accepted values: master, resource

Required: False
Position: Named
Default value: Master
Accept pipeline input: False
Accept wildcard characters: False
```

### -Media

Not Required to be set when attaching raw media.
This is the URL link or file path where the attachment resides.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewId

This is the new Id of the attachment if renaming the attachment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionKey

The partition keys for the collection that the attachment is in.
Must be included if and only if the collection is created with
a partitionKey definition.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slug

The name of the attachment.
This is only required when raw media is submitted to the Azure Cosmos DB attachment storage.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
