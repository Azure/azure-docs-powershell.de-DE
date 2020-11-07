---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/restore-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: f93a173e79cb34c5603ce58fc3e03c92869a5d01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842683"
---
# <span data-ttu-id="8ea7b-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="8ea7b-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="8ea7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ea7b-102">SYNOPSIS</span></span>

## <span data-ttu-id="8ea7b-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ea7b-103">SYNTAX</span></span>

### <span data-ttu-id="8ea7b-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="8ea7b-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="8ea7b-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="8ea7b-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="8ea7b-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ea7b-106">DESCRIPTION</span></span>
<span data-ttu-id="8ea7b-107">Das Cmdlet **Restore-AzWebAppBackup** stellt eine Azure Web App-Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="8ea7b-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ea7b-108">EXAMPLES</span></span>

### <span data-ttu-id="8ea7b-109">1:</span><span class="sxs-lookup"><span data-stu-id="8ea7b-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="8ea7b-110">Stellt eine Sicherung des angegebenen app-ContosoWebApp wieder her, die sich innerhalb der Ressourcengruppe Default-Web-westus im BLOB "myblob" befindet unter https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="8ea7b-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="8ea7b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ea7b-111">PARAMETERS</span></span>

### <span data-ttu-id="8ea7b-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8ea7b-112">-AppServicePlan</span></span>
<span data-ttu-id="8ea7b-113">Der Name des App-Dienstplans für die wiederhergestellte app.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="8ea7b-114">Wenn die Funktion leer bleibt, wird der aktuelle App-Service Plan der APP verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-114">If left empty, the app's current App Service Plan is used.</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ea7b-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="8ea7b-115">-BlobName</span></span>
<span data-ttu-id="8ea7b-116">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="8ea7b-116">Blob Name</span></span>

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

### <span data-ttu-id="8ea7b-117">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="8ea7b-117">-Databases</span></span>
<span data-ttu-id="8ea7b-118">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="8ea7b-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="8ea7b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ea7b-119">-DefaultProfile</span></span>
<span data-ttu-id="8ea7b-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ea7b-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="8ea7b-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="8ea7b-122">Option "in Konflikt stehende hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="8ea7b-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="8ea7b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8ea7b-123">-Name</span></span>
<span data-ttu-id="8ea7b-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="8ea7b-124">WebApp Name</span></span>

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

### <span data-ttu-id="8ea7b-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="8ea7b-125">-Overwrite</span></span>
<span data-ttu-id="8ea7b-126">Option "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="8ea7b-126">Overwrite Option</span></span>

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

### <span data-ttu-id="8ea7b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ea7b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ea7b-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="8ea7b-128">Resource Group Name</span></span>

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

### <span data-ttu-id="8ea7b-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="8ea7b-129">-Slot</span></span>
<span data-ttu-id="8ea7b-130">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="8ea7b-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="8ea7b-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="8ea7b-131">-StorageAccountUrl</span></span>
<span data-ttu-id="8ea7b-132">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="8ea7b-132">Storage Account Url</span></span>

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

### <span data-ttu-id="8ea7b-133">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="8ea7b-133">-WebApp</span></span>
<span data-ttu-id="8ea7b-134">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="8ea7b-134">WebApp Object</span></span>

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

### <span data-ttu-id="8ea7b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ea7b-135">CommonParameters</span></span>
<span data-ttu-id="8ea7b-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ea7b-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ea7b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ea7b-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ea7b-138">INPUTS</span></span>

### <span data-ttu-id="8ea7b-139">Website</span><span class="sxs-lookup"><span data-stu-id="8ea7b-139">Site</span></span>
<span data-ttu-id="8ea7b-140">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8ea7b-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="8ea7b-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ea7b-141">OUTPUTS</span></span>

## <span data-ttu-id="8ea7b-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ea7b-142">NOTES</span></span>

## <span data-ttu-id="8ea7b-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ea7b-143">RELATED LINKS</span></span>

