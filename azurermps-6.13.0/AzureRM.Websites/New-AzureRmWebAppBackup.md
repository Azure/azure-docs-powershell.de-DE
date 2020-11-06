---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: a4cdec386269bbda7ceb34ec8731c51d7eb1fc44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502797"
---
# <span data-ttu-id="c4225-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c4225-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="c4225-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4225-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4225-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4225-103">SYNTAX</span></span>

### <span data-ttu-id="c4225-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="c4225-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="c4225-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="c4225-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="c4225-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4225-106">DESCRIPTION</span></span>
<span data-ttu-id="c4225-107">Das Cmdlet **New-AzureRmWebAppBackup** erstellt eine Azure Web App-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="c4225-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="c4225-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4225-108">EXAMPLES</span></span>

### <span data-ttu-id="c4225-109">1:</span><span class="sxs-lookup"><span data-stu-id="c4225-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="c4225-110">Erstellt eine Sicherungskopie der angegebenen app-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe befindet-Web-westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="c4225-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="c4225-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4225-111">PARAMETERS</span></span>

### <span data-ttu-id="c4225-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="c4225-112">-BackupName</span></span>
<span data-ttu-id="c4225-113">Sicherungs Name</span><span class="sxs-lookup"><span data-stu-id="c4225-113">Backup Name</span></span>

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

### <span data-ttu-id="c4225-114">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="c4225-114">-Databases</span></span>
<span data-ttu-id="c4225-115">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c4225-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="c4225-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4225-116">-DefaultProfile</span></span>
<span data-ttu-id="c4225-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4225-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4225-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c4225-118">-Name</span></span>
<span data-ttu-id="c4225-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="c4225-119">WebApp Name</span></span>

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

### <span data-ttu-id="c4225-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4225-120">-ResourceGroupName</span></span>
<span data-ttu-id="c4225-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="c4225-121">Resource Group Name</span></span>

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

### <span data-ttu-id="c4225-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="c4225-122">-Slot</span></span>
<span data-ttu-id="c4225-123">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="c4225-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="c4225-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="c4225-124">-StorageAccountUrl</span></span>
<span data-ttu-id="c4225-125">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="c4225-125">Storage Account Url</span></span>

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

### <span data-ttu-id="c4225-126">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="c4225-126">-WebApp</span></span>
<span data-ttu-id="c4225-127">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="c4225-127">WebApp Object</span></span>

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

### <span data-ttu-id="c4225-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4225-128">CommonParameters</span></span>
<span data-ttu-id="c4225-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4225-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4225-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4225-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4225-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4225-131">INPUTS</span></span>

### <span data-ttu-id="c4225-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c4225-132">System.String</span></span>

### <span data-ttu-id="c4225-133">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="c4225-133">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="c4225-134">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="c4225-134">Parameters: WebApp (ByValue)</span></span>

### <span data-ttu-id="c4225-135">Microsoft. Azure. Management. Websites. Models. DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="c4225-135">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting[]</span></span>

## <span data-ttu-id="c4225-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4225-136">OUTPUTS</span></span>

### <span data-ttu-id="c4225-137">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="c4225-137">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="c4225-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4225-138">NOTES</span></span>

## <span data-ttu-id="c4225-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4225-139">RELATED LINKS</span></span>
