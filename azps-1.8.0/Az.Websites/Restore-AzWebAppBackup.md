---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: DC400E32-CAB9-4354-99B2-ABA4AA776030
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restore-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restore-AzWebAppBackup.md
ms.openlocfilehash: 94fbc71db34ca0abc6a27130dc166318794e271a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658509"
---
# <span data-ttu-id="57c06-101">Restore-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="57c06-101">Restore-AzWebAppBackup</span></span>

## <span data-ttu-id="57c06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57c06-102">SYNOPSIS</span></span>

## <span data-ttu-id="57c06-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="57c06-103">SYNTAX</span></span>

### <span data-ttu-id="57c06-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="57c06-104">FromResourceName</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite]
 [<CommonParameters>]
```

### <span data-ttu-id="57c06-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="57c06-105">FromWebApp</span></span>
```
Restore-AzWebAppBackup [-AppServicePlan <String>] [-Databases <DatabaseBackupSetting[]>]
 [-IgnoreConflictingHostNames] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-BlobName] <String> [-Overwrite] [<CommonParameters>]
```

## <span data-ttu-id="57c06-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57c06-106">DESCRIPTION</span></span>
<span data-ttu-id="57c06-107">Das Cmdlet **Restore-AzWebAppBackup** stellt eine Azure Web App-Sicherung wieder her.</span><span class="sxs-lookup"><span data-stu-id="57c06-107">The **Restore-AzWebAppBackup** cmdlet restores an Azure Web App Backup.</span></span>

## <span data-ttu-id="57c06-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57c06-108">EXAMPLES</span></span>

### <span data-ttu-id="57c06-109">1:</span><span class="sxs-lookup"><span data-stu-id="57c06-109">1:</span></span>
```
PS C:\> Restore-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net" -BlobName "myBlob"
```

<span data-ttu-id="57c06-110">Stellt eine Sicherung des angegebenen app-ContosoWebApp wieder her, die sich innerhalb der Ressourcengruppe Default-Web-westus im BLOB "myblob" befindet unter https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="57c06-110">Restores a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in blob "myBlob" located at https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="57c06-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="57c06-111">PARAMETERS</span></span>

### <span data-ttu-id="57c06-112">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="57c06-112">-AppServicePlan</span></span>
<span data-ttu-id="57c06-113">Der Name des App-Dienstplans für die wiederhergestellte app.</span><span class="sxs-lookup"><span data-stu-id="57c06-113">The name of the App Service Plan for the restored app.</span></span> <span data-ttu-id="57c06-114">Wenn die Funktion leer bleibt, wird der aktuelle App-Service Plan der APP verwendet.</span><span class="sxs-lookup"><span data-stu-id="57c06-114">If left empty, the app's current App Service Plan is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="57c06-115">-BlobName</span></span>
<span data-ttu-id="57c06-116">BLOB-Name</span><span class="sxs-lookup"><span data-stu-id="57c06-116">Blob Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-117">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="57c06-117">-Databases</span></span>
<span data-ttu-id="57c06-118">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="57c06-118">Databases of type DatabaseBackupSetting[]</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c06-119">-DefaultProfile</span></span>
<span data-ttu-id="57c06-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57c06-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-121">-IgnoreConflictingHostNames</span><span class="sxs-lookup"><span data-stu-id="57c06-121">-IgnoreConflictingHostNames</span></span>
<span data-ttu-id="57c06-122">Option "in Konflikt stehende hostnames ignorieren"</span><span class="sxs-lookup"><span data-stu-id="57c06-122">Ignore Conflicting HostNames Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-123">-Name</span><span class="sxs-lookup"><span data-stu-id="57c06-123">-Name</span></span>
<span data-ttu-id="57c06-124">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="57c06-124">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-125">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="57c06-125">-Overwrite</span></span>
<span data-ttu-id="57c06-126">Option "überschreiben"</span><span class="sxs-lookup"><span data-stu-id="57c06-126">Overwrite Option</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c06-127">-ResourceGroupName</span></span>
<span data-ttu-id="57c06-128">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="57c06-128">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-129">-Slot</span><span class="sxs-lookup"><span data-stu-id="57c06-129">-Slot</span></span>
<span data-ttu-id="57c06-130">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="57c06-130">WebApp Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-131">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="57c06-131">-StorageAccountUrl</span></span>
<span data-ttu-id="57c06-132">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="57c06-132">Storage Account Url</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-133">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="57c06-133">-WebApp</span></span>
<span data-ttu-id="57c06-134">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="57c06-134">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: FromWebApp
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c06-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c06-135">CommonParameters</span></span>
<span data-ttu-id="57c06-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c06-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c06-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c06-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c06-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57c06-138">INPUTS</span></span>

### <span data-ttu-id="57c06-139">System. String</span><span class="sxs-lookup"><span data-stu-id="57c06-139">System.String</span></span>

### <span data-ttu-id="57c06-140">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="57c06-140">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

### <span data-ttu-id="57c06-141">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="57c06-141">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="57c06-142">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="57c06-142">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="57c06-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57c06-143">OUTPUTS</span></span>

### <span data-ttu-id="57c06-144">System. void</span><span class="sxs-lookup"><span data-stu-id="57c06-144">System.Void</span></span>

## <span data-ttu-id="57c06-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="57c06-145">NOTES</span></span>

## <span data-ttu-id="57c06-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57c06-146">RELATED LINKS</span></span>
