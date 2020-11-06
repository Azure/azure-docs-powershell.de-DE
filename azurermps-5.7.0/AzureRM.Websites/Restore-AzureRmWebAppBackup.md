---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Restore-AzureRmWebAppBackup.md
ms.openlocfilehash: c68d9afb7c9498bbf734abcc376e6f123ebb8ac3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501285"
---
# <span data-ttu-id="b0b8c-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="b0b8c-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="b0b8c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0b8c-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0b8c-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0b8c-103">SYNTAX</span></span>

### <span data-ttu-id="b0b8c-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="b0b8c-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

### <span data-ttu-id="b0b8c-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="b0b8c-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-Databases <DatabaseBackupSetting[]>] [-IgnoreConflictingHostNames]
 [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String>
 [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="b0b8c-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0b8c-106">DESCRIPTION</span></span>
<span data-ttu-id="b0b8c-107">Das Cmdlet **Restore-AzureRmWebAppBackup** stellt eine Azure Web App-Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="b0b8c-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="b0b8c-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0b8c-108">EXAMPLES</span></span>

### <span data-ttu-id="b0b8c-109">1:</span><span class="sxs-lookup"><span data-stu-id="b0b8c-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="b0b8c-110">Stellt eine Sicherung des angegebenen app-ContosoWebApp wieder her, die sich innerhalb der Ressourcengruppe Default-Web-westus im BLOB "myblob" befindet unter https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="b0b8c-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="b0b8c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0b8c-111">PARAMETERS</span></span>

### <span data-ttu-id="b0b8c-112">-Blobname</span><span class="sxs-lookup"><span data-stu-id="b0b8c-112">-BlobName</span></span>
<span data-ttu-id="b0b8c-113">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="b0b8c-113">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-114">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="b0b8c-114">-Databases</span></span>
<span data-ttu-id="b0b8c-115">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="b0b8c-115">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0b8c-116">-DefaultProfile</span></span>
<span data-ttu-id="b0b8c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0b8c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-118">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="b0b8c-118">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="b0b8c-119">Option "in Konflikt stehende hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="b0b8c-119">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b0b8c-120">-Name</span></span>
<span data-ttu-id="b0b8c-121">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="b0b8c-121">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-122">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="b0b8c-122">-Overwrite</span></span>
<span data-ttu-id="b0b8c-123">Option "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="b0b8c-123">Overwrite Option</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="b0b8c-125">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="b0b8c-125">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-126">-Slot</span><span class="sxs-lookup"><span data-stu-id="b0b8c-126">-Slot</span></span>
<span data-ttu-id="b0b8c-127">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="b0b8c-127">WebApp Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-128">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="b0b8c-128">-StorageAccountUrl</span></span>
<span data-ttu-id="b0b8c-129">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="b0b8c-129">Storage Account Url</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-130">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="b0b8c-130">-WebApp</span></span>
<span data-ttu-id="b0b8c-131">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="b0b8c-131">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b0b8c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b8c-132">CommonParameters</span></span>
<span data-ttu-id="b0b8c-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0b8c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b8c-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b8c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b8c-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0b8c-135">INPUTS</span></span>

### <span data-ttu-id="b0b8c-136">Website</span><span class="sxs-lookup"><span data-stu-id="b0b8c-136">Site</span></span>
<span data-ttu-id="b0b8c-137">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0b8c-137">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="b0b8c-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0b8c-138">OUTPUTS</span></span>

## <span data-ttu-id="b0b8c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0b8c-139">NOTES</span></span>

## <span data-ttu-id="b0b8c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0b8c-140">RELATED LINKS</span></span>

