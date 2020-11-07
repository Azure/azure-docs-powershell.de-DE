---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/restore-azurermwebappbackup
schema: 2.0.0
ms.openlocfilehash: 9c28d9235eefe6c4f33537115b548137c5bc6c88
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850203"
---
# <span data-ttu-id="d11dc-101">Restore-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="d11dc-101">Restore-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="d11dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d11dc-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d11dc-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="d11dc-103">SYNTAX</span></span>

### <span data-ttu-id="d11dc-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="d11dc-104">FromResourceName</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="d11dc-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="d11dc-105">FromWebApp</span></span>
```
Restore-AzureRmWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="d11dc-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d11dc-106">DESCRIPTION</span></span>
<span data-ttu-id="d11dc-107">Das Cmdlet **Restore-AzureRmWebAppBackup** stellt eine Azure Web App-Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="d11dc-107">The **Restore-AzureRmWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="d11dc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d11dc-108">EXAMPLES</span></span>

### <span data-ttu-id="d11dc-109">1:</span><span class="sxs-lookup"><span data-stu-id="d11dc-109">1:</span></span>
```
PS C:\> Restore-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="d11dc-110">Stellt eine Sicherung des angegebenen app-ContosoWebApp wieder her, die sich innerhalb der Ressourcengruppe Default-Web-westus im BLOB "myblob" befindet unter https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="d11dc-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="d11dc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d11dc-111">PARAMETERS</span></span>

### <span data-ttu-id="d11dc-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d11dc-112">-AppServicePlan</span></span>
<span data-ttu-id="d11dc-113">Der Name des App-Dienstplans für die wiederhergestellte app.</span><span class="sxs-lookup"><span data-stu-id="d11dc-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="d11dc-114">Wenn die Funktion leer bleibt, wird der aktuelle App-Service Plan der APP verwendet.</span><span class="sxs-lookup"><span data-stu-id="d11dc-114">If left empty, the app's current App Service Plan is used.</span></span>
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

### <span data-ttu-id="d11dc-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="d11dc-115">-BlobName</span></span>
<span data-ttu-id="d11dc-116">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="d11dc-116">Blob Name</span></span>

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

### <span data-ttu-id="d11dc-117">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="d11dc-117">-Databases</span></span>
<span data-ttu-id="d11dc-118">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="d11dc-118">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="d11dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11dc-119">-DefaultProfile</span></span>
<span data-ttu-id="d11dc-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d11dc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d11dc-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="d11dc-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="d11dc-122">Option "in Konflikt stehende hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="d11dc-122">Ignore Conflicting HostNames Option</span></span>

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

### <span data-ttu-id="d11dc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d11dc-123">-Name</span></span>
<span data-ttu-id="d11dc-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="d11dc-124">WebApp Name</span></span>

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

### <span data-ttu-id="d11dc-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="d11dc-125">-Overwrite</span></span>
<span data-ttu-id="d11dc-126">Option "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="d11dc-126">Overwrite Option</span></span>

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

### <span data-ttu-id="d11dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d11dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="d11dc-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="d11dc-128">Resource Group Name</span></span>

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

### <span data-ttu-id="d11dc-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="d11dc-129">-Slot</span></span>
<span data-ttu-id="d11dc-130">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="d11dc-130">WebApp Slot Name</span></span>

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

### <span data-ttu-id="d11dc-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="d11dc-131">-StorageAccountUrl</span></span>
<span data-ttu-id="d11dc-132">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="d11dc-132">Storage Account Url</span></span>

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

### <span data-ttu-id="d11dc-133">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="d11dc-133">-WebApp</span></span>
<span data-ttu-id="d11dc-134">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="d11dc-134">WebApp Object</span></span>

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

### <span data-ttu-id="d11dc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11dc-135">CommonParameters</span></span>
<span data-ttu-id="d11dc-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11dc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11dc-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d11dc-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11dc-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d11dc-138">INPUTS</span></span>

### <span data-ttu-id="d11dc-139">Website</span><span class="sxs-lookup"><span data-stu-id="d11dc-139">Site</span></span>
<span data-ttu-id="d11dc-140">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="d11dc-140">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="d11dc-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d11dc-141">OUTPUTS</span></span>

## <span data-ttu-id="d11dc-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="d11dc-142">NOTES</span></span>

## <span data-ttu-id="d11dc-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d11dc-143">RELATED LINKS</span></span>

