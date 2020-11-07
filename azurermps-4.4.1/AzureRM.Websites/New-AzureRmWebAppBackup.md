---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppBackup.md
ms.openlocfilehash: 03c9b54dd83f4689f763ef45e0f9a7c0d8b89672
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664953"
---
# <span data-ttu-id="1959d-101">New-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1959d-101">New-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="1959d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1959d-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1959d-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="1959d-103">SYNTAX</span></span>

### <span data-ttu-id="1959d-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1959d-104">FromResourceName</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="1959d-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1959d-105">FromWebApp</span></span>
```
New-AzureRmWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="1959d-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1959d-106">DESCRIPTION</span></span>
<span data-ttu-id="1959d-107">Das Cmdlet **New-AzureRmWebAppBackup** erstellt eine Azure Web App-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="1959d-107">The **New-AzureRmWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="1959d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1959d-108">EXAMPLES</span></span>

### <span data-ttu-id="1959d-109">1:</span><span class="sxs-lookup"><span data-stu-id="1959d-109">1:</span></span>
```
PS C:\> New-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="1959d-110">Erstellt eine Sicherungskopie der angegebenen app-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe befindet-Web-westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="1959d-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="1959d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1959d-111">PARAMETERS</span></span>

### <span data-ttu-id="1959d-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="1959d-112">-BackupName</span></span>
<span data-ttu-id="1959d-113">Sicherungs Name</span><span class="sxs-lookup"><span data-stu-id="1959d-113">Backup Name</span></span>

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

### <span data-ttu-id="1959d-114">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="1959d-114">-Databases</span></span>
<span data-ttu-id="1959d-115">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="1959d-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="1959d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1959d-116">-Name</span></span>
<span data-ttu-id="1959d-117">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="1959d-117">WebApp Name</span></span>

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

### <span data-ttu-id="1959d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1959d-118">-ResourceGroupName</span></span>
<span data-ttu-id="1959d-119">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="1959d-119">Resource Group Name</span></span>

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

### <span data-ttu-id="1959d-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="1959d-120">-Slot</span></span>
<span data-ttu-id="1959d-121">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="1959d-121">WebApp Slot Name</span></span>

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

### <span data-ttu-id="1959d-122">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="1959d-122">-StorageAccountUrl</span></span>
<span data-ttu-id="1959d-123">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="1959d-123">Storage Account Url</span></span>

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

### <span data-ttu-id="1959d-124">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="1959d-124">-WebApp</span></span>
<span data-ttu-id="1959d-125">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="1959d-125">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1959d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1959d-126">-DefaultProfile</span></span>
<span data-ttu-id="1959d-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1959d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1959d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1959d-128">CommonParameters</span></span>
<span data-ttu-id="1959d-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1959d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1959d-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1959d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1959d-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1959d-131">INPUTS</span></span>

### <span data-ttu-id="1959d-132">Website</span><span class="sxs-lookup"><span data-stu-id="1959d-132">Site</span></span>
<span data-ttu-id="1959d-133">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="1959d-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1959d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1959d-134">OUTPUTS</span></span>

### <span data-ttu-id="1959d-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="1959d-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="1959d-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="1959d-136">NOTES</span></span>

## <span data-ttu-id="1959d-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1959d-137">RELATED LINKS</span></span>

