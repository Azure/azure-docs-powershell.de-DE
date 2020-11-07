---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: D3FE0440-C663-4379-8F5F-2E66EF024E5D
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppBackup.md
ms.openlocfilehash: a01c49ac6591cfec7d8087d664ba61ddd825ac5e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842751"
---
# <span data-ttu-id="02a31-101">New-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="02a31-101">New-AzWebAppBackup</span></span>

## <span data-ttu-id="02a31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02a31-102">SYNOPSIS</span></span>

## <span data-ttu-id="02a31-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="02a31-103">SYNTAX</span></span>

### <span data-ttu-id="02a31-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="02a31-104">FromResourceName</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-ResourceGroupName] <String> [-Name] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [-StorageAccountUrl] <String>
 [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

### <span data-ttu-id="02a31-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="02a31-105">FromWebApp</span></span>
```
New-AzWebAppBackup [[-BackupName] <String>] [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [-StorageAccountUrl] <String> [-Databases <DatabaseBackupSetting[]>] [<CommonParameters>]
```

## <span data-ttu-id="02a31-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02a31-106">DESCRIPTION</span></span>
<span data-ttu-id="02a31-107">Das Cmdlet **New-AzWebAppBackup** erstellt eine Azure Web App-Sicherung.</span><span class="sxs-lookup"><span data-stu-id="02a31-107">The **New-AzWebAppBackup** cmdlet creates an Azure Web App Backup.</span></span>

## <span data-ttu-id="02a31-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02a31-108">EXAMPLES</span></span>

### <span data-ttu-id="02a31-109">1:</span><span class="sxs-lookup"><span data-stu-id="02a31-109">1:</span></span>
```
PS C:\> New-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -StorageAccountUrl "https://storageaccount.file.core.windows.net"
```

<span data-ttu-id="02a31-110">Erstellt eine Sicherungskopie der angegebenen app-ContosoWebApp, die sich in der standardmäßigen Ressourcengruppe befindet-Web-westus in https://storageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="02a31-110">Creates a backup of the specified app ContosoWebApp that is within resource group Default-Web-WestUS in https://storageaccount.file.core.windows.net</span></span>

## <span data-ttu-id="02a31-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="02a31-111">PARAMETERS</span></span>

### <span data-ttu-id="02a31-112">-BackupName</span><span class="sxs-lookup"><span data-stu-id="02a31-112">-BackupName</span></span>
<span data-ttu-id="02a31-113">Sicherungs Name</span><span class="sxs-lookup"><span data-stu-id="02a31-113">Backup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a31-114">-Datenbanken</span><span class="sxs-lookup"><span data-stu-id="02a31-114">-Databases</span></span>
<span data-ttu-id="02a31-115">Datenbanken vom Typ DatabaseBackupSetting []</span><span class="sxs-lookup"><span data-stu-id="02a31-115">Databases of type DatabaseBackupSetting[]</span></span>

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

### <span data-ttu-id="02a31-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a31-116">-DefaultProfile</span></span>
<span data-ttu-id="02a31-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02a31-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a31-118">-Name</span><span class="sxs-lookup"><span data-stu-id="02a31-118">-Name</span></span>
<span data-ttu-id="02a31-119">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="02a31-119">WebApp Name</span></span>

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

### <span data-ttu-id="02a31-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a31-120">-ResourceGroupName</span></span>
<span data-ttu-id="02a31-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="02a31-121">Resource Group Name</span></span>

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

### <span data-ttu-id="02a31-122">-Slot</span><span class="sxs-lookup"><span data-stu-id="02a31-122">-Slot</span></span>
<span data-ttu-id="02a31-123">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="02a31-123">WebApp Slot Name</span></span>

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

### <span data-ttu-id="02a31-124">-StorageAccountUrl</span><span class="sxs-lookup"><span data-stu-id="02a31-124">-StorageAccountUrl</span></span>
<span data-ttu-id="02a31-125">Speicherkonto-URL</span><span class="sxs-lookup"><span data-stu-id="02a31-125">Storage Account Url</span></span>

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

### <span data-ttu-id="02a31-126">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="02a31-126">-WebApp</span></span>
<span data-ttu-id="02a31-127">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="02a31-127">WebApp Object</span></span>

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

### <span data-ttu-id="02a31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a31-128">CommonParameters</span></span>
<span data-ttu-id="02a31-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a31-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a31-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a31-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02a31-131">INPUTS</span></span>

### <span data-ttu-id="02a31-132">Website</span><span class="sxs-lookup"><span data-stu-id="02a31-132">Site</span></span>
<span data-ttu-id="02a31-133">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02a31-133">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="02a31-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02a31-134">OUTPUTS</span></span>

### <span data-ttu-id="02a31-135">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="02a31-135">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="02a31-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="02a31-136">NOTES</span></span>

## <span data-ttu-id="02a31-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02a31-137">RELATED LINKS</span></span>

