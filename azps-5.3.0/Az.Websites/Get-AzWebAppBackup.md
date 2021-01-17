---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EAAF615B-6139-438B-A2FD-6966E72B3AA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppBackup.md
ms.openlocfilehash: e8c3f7543062613527e7f52be2cd6493f53c5f60
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380776"
---
# <span data-ttu-id="e3861-101">Get-AzWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e3861-101">Get-AzWebAppBackup</span></span>

## <span data-ttu-id="e3861-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3861-102">SYNOPSIS</span></span>

## <span data-ttu-id="e3861-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3861-103">SYNTAX</span></span>

### <span data-ttu-id="e3861-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="e3861-104">FromResourceName</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3861-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="e3861-105">FromWebApp</span></span>
```
Get-AzWebAppBackup [-BackupId] <String> [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3861-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3861-106">DESCRIPTION</span></span>
<span data-ttu-id="e3861-107">Das **Cmdlet "Get-AzWebAppBackup"** ruft die angegebene Sicherung einer Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="e3861-107">The **Get-AzWebAppBackup** cmdlet gets the specified backup of an Azure Web App.</span></span>

## <span data-ttu-id="e3861-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3861-108">EXAMPLES</span></span>

### <span data-ttu-id="e3861-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e3861-109">Example 1</span></span>
```powershell
PS C:\>Get-AzWebAppBackup -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -BackupId "12345"
```

<span data-ttu-id="e3861-110">Dieser Befehl ruft die Sicherung mit der ID "12345" aus der Web App namens WebAppStandard ab, die zur Ressourcengruppe "Default-Web-WestUS" gehört.</span><span class="sxs-lookup"><span data-stu-id="e3861-110">This command gets the backup with ID "12345" from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="e3861-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3861-111">PARAMETERS</span></span>

### <span data-ttu-id="e3861-112">-BackupId</span><span class="sxs-lookup"><span data-stu-id="e3861-112">-BackupId</span></span>
<span data-ttu-id="e3861-113">Sicherungs-ID</span><span class="sxs-lookup"><span data-stu-id="e3861-113">Backup Id</span></span>

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

### <span data-ttu-id="e3861-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3861-114">-DefaultProfile</span></span>
<span data-ttu-id="e3861-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3861-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3861-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e3861-116">-Name</span></span>
<span data-ttu-id="e3861-117">Webapp Name</span><span class="sxs-lookup"><span data-stu-id="e3861-117">Webapp Name</span></span>

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

### <span data-ttu-id="e3861-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3861-118">-ResourceGroupName</span></span>
<span data-ttu-id="e3861-119">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="e3861-119">Resource Group Name</span></span>

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

### <span data-ttu-id="e3861-120">-Slot</span><span class="sxs-lookup"><span data-stu-id="e3861-120">-Slot</span></span>
<span data-ttu-id="e3861-121">Slot Name</span><span class="sxs-lookup"><span data-stu-id="e3861-121">Slot Name</span></span>

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

### <span data-ttu-id="e3861-122">-WebApp</span><span class="sxs-lookup"><span data-stu-id="e3861-122">-WebApp</span></span>
<span data-ttu-id="e3861-123">Piped WebApp</span><span class="sxs-lookup"><span data-stu-id="e3861-123">Piped WebApp</span></span>

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

### <span data-ttu-id="e3861-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3861-124">CommonParameters</span></span>
<span data-ttu-id="e3861-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3861-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3861-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3861-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3861-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3861-127">INPUTS</span></span>

### <span data-ttu-id="e3861-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e3861-128">System.String</span></span>

### <span data-ttu-id="e3861-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="e3861-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="e3861-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3861-130">OUTPUTS</span></span>

### <span data-ttu-id="e3861-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span><span class="sxs-lookup"><span data-stu-id="e3861-131">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackup</span></span>

## <span data-ttu-id="e3861-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3861-132">NOTES</span></span>

## <span data-ttu-id="e3861-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3861-133">RELATED LINKS</span></span>
