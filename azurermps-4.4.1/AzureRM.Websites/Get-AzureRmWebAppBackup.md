---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackup.md
ms.openlocfilehash: b88386077cd1a1e7b934b2a05126f00fa76bec18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499910"
---
# <span data-ttu-id="46b34-101">Get-AzureRmWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="46b34-101">Get-AzureRmWebAppBackup</span></span>

## <span data-ttu-id="46b34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="46b34-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46b34-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="46b34-103">SYNTAX</span></span>

### <span data-ttu-id="46b34-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="46b34-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46b34-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="46b34-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackup [-BackupId] <String> [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="46b34-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46b34-106">DESCRIPTION</span></span>
<span data-ttu-id="46b34-107">Das Cmdlet " **Get-AzureRmWebAppBackup** " Ruft die angegebene Sicherung einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="46b34-107">The **Get-AzureRmWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="46b34-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="46b34-108">EXAMPLES</span></span>

### <span data-ttu-id="46b34-109">1:</span><span class="sxs-lookup"><span data-stu-id="46b34-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="46b34-110">Dieser Befehl ruft die Sicherung mit der ID "12345" aus der Web-App mit dem Namen WebAppStandard ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="46b34-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="46b34-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46b34-111">PARAMETERS</span></span>

### <span data-ttu-id="46b34-112">-Backup-Nr.</span><span class="sxs-lookup"><span data-stu-id="46b34-112">-BackupId</span></span>
<span data-ttu-id="46b34-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="46b34-113">Backup Id</span></span>

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

### <span data-ttu-id="46b34-114">-Name</span><span class="sxs-lookup"><span data-stu-id="46b34-114">-Name</span></span>
<span data-ttu-id="46b34-115">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="46b34-115">Webapp Name</span></span>

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

### <span data-ttu-id="46b34-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46b34-116">-ResourceGroupName</span></span>
<span data-ttu-id="46b34-117">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="46b34-117">Resource Group Name</span></span>

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

### <span data-ttu-id="46b34-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="46b34-118">-Slot</span></span>
<span data-ttu-id="46b34-119">Name des Steckplatzes</span><span class="sxs-lookup"><span data-stu-id="46b34-119">Slot Name</span></span>

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

### <span data-ttu-id="46b34-120">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="46b34-120">-WebApp</span></span>
<span data-ttu-id="46b34-121">Pipelining</span><span class="sxs-lookup"><span data-stu-id="46b34-121">Piped WebApp</span></span>

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

### <span data-ttu-id="46b34-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46b34-122">-DefaultProfile</span></span>
<span data-ttu-id="46b34-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="46b34-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46b34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46b34-124">CommonParameters</span></span>
<span data-ttu-id="46b34-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46b34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46b34-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46b34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46b34-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="46b34-127">INPUTS</span></span>

### <span data-ttu-id="46b34-128">Website</span><span class="sxs-lookup"><span data-stu-id="46b34-128">Site</span></span>
<span data-ttu-id="46b34-129">Der Parameter "WebStart" akzeptiert den Wert vom Typ "Website" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="46b34-129">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="46b34-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="46b34-130">OUTPUTS</span></span>

### <span data-ttu-id="46b34-131">Microsoft. Azure. Commands. webapps. Cmdlets. webapps. AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="46b34-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="46b34-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="46b34-132">NOTES</span></span>

## <span data-ttu-id="46b34-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="46b34-133">RELATED LINKS</span></span>

