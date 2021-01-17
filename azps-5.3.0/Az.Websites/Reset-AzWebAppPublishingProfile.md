---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460364"
---
# <span data-ttu-id="9e328-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="9e328-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="9e328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e328-102">SYNOPSIS</span></span>

## <span data-ttu-id="9e328-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e328-103">SYNTAX</span></span>

### <span data-ttu-id="9e328-104">S1</span><span class="sxs-lookup"><span data-stu-id="9e328-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9e328-105">S2</span><span class="sxs-lookup"><span data-stu-id="9e328-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e328-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e328-106">DESCRIPTION</span></span>
<span data-ttu-id="9e328-107">Das **Cmdlet "Reset-AzWebAppPublishingProfile"** setzt das Veröffentlichungsprofil für die angegebene Web App zurück.</span><span class="sxs-lookup"><span data-stu-id="9e328-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="9e328-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9e328-108">EXAMPLES</span></span>

### <span data-ttu-id="9e328-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9e328-109">Example 1</span></span>

<span data-ttu-id="9e328-110">Im folgenden Beispiel wird das Veröffentlichungsprofil für die Web App-IpRule zurückgesetzt, die der Ressourcengruppe "MyResourceGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9e328-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="9e328-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e328-111">PARAMETERS</span></span>

### <span data-ttu-id="9e328-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e328-112">-DefaultProfile</span></span>
<span data-ttu-id="9e328-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9e328-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e328-114">-Name</span><span class="sxs-lookup"><span data-stu-id="9e328-114">-Name</span></span>
<span data-ttu-id="9e328-115">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="9e328-115">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e328-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e328-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e328-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="9e328-117">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e328-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="9e328-118">-WebApp</span></span>
<span data-ttu-id="9e328-119">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e328-119">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9e328-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e328-120">CommonParameters</span></span>
<span data-ttu-id="9e328-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e328-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e328-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e328-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e328-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9e328-123">INPUTS</span></span>

### <span data-ttu-id="9e328-124">System.String</span><span class="sxs-lookup"><span data-stu-id="9e328-124">System.String</span></span>

### <span data-ttu-id="9e328-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="9e328-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="9e328-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9e328-126">OUTPUTS</span></span>

### <span data-ttu-id="9e328-127">System.String</span><span class="sxs-lookup"><span data-stu-id="9e328-127">System.String</span></span>

## <span data-ttu-id="9e328-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9e328-128">NOTES</span></span>

## <span data-ttu-id="9e328-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9e328-129">RELATED LINKS</span></span>
