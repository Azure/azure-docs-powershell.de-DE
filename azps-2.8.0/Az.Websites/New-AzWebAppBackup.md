---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: 2ef015c3f793dd4636632f17568feb9aaf1b5ad2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93827183"
---
# <span data-ttu-id="f9e83-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f9e83-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="f9e83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9e83-102">SYNOPSIS</span></span>

## <span data-ttu-id="f9e83-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9e83-103">SYNTAX</span></span>

### <span data-ttu-id="f9e83-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="f9e83-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="f9e83-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="f9e83-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="f9e83-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9e83-106">DESCRIPTION</span></span>
<span data-ttu-id="f9e83-107">Das Cmdlet **New-AzWebAppBackup** erstellt eine Azure Web App-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="f9e83-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="f9e83-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9e83-108">EXAMPLES</span></span>

### <span data-ttu-id="f9e83-109">1:</span><span class="sxs-lookup"><span data-stu-id="f9e83-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="f9e83-110">Erstellt eine Sicherungskopie der angegebenen app-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe befindet-Web-westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="f9e83-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="f9e83-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e83-111">PARAMETERS</span></span>

### <span data-ttu-id="f9e83-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="f9e83-112">-BackupName</span></span>
<span data-ttu-id="f9e83-113">Sicherungs Name</span><span class="sxs-lookup"><span data-stu-id="f9e83-113">Backup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9e83-114">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="f9e83-114">-Databases</span></span>
<span data-ttu-id="f9e83-115">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f9e83-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="f9e83-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e83-116">-DefaultProfile</span></span>
<span data-ttu-id="f9e83-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9e83-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9e83-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f9e83-118">-Name</span></span>
<span data-ttu-id="f9e83-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f9e83-119">WebApp Name</span></span>

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

### <span data-ttu-id="f9e83-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e83-120">-ResourceGroupName</span></span>
<span data-ttu-id="f9e83-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f9e83-121">Resource Group Name</span></span>

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

### <span data-ttu-id="f9e83-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="f9e83-122">-Slot</span></span>
<span data-ttu-id="f9e83-123">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="f9e83-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="f9e83-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="f9e83-124">-StorageAccountUrl</span></span>
<span data-ttu-id="f9e83-125">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="f9e83-125">Storage Account Url</span></span>

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

### <span data-ttu-id="f9e83-126">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="f9e83-126">-WebApp</span></span>
<span data-ttu-id="f9e83-127">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="f9e83-127">WebApp Object</span></span>

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

### <span data-ttu-id="f9e83-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e83-128">CommonParameters</span></span>
<span data-ttu-id="f9e83-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9e83-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e83-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9e83-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e83-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9e83-131">INPUTS</span></span>

### <span data-ttu-id="f9e83-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f9e83-132">System.String</span></span>

### <span data-ttu-id="f9e83-133">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="f9e83-133">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

### <span data-ttu-id="f9e83-134">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="f9e83-134">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="f9e83-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9e83-135">OUTPUTS</span></span>

### <span data-ttu-id="f9e83-136">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="f9e83-136">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="f9e83-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9e83-137">NOTES</span></span>

## <span data-ttu-id="f9e83-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9e83-138">RELATED LINKS</span></span>
