---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 84C861B2-DCB3-47F0-8589-BB3172C6E1EC
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/reset-azwebapppublishingprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Reset-AzWebAppPublishingProfile.md
ms.openlocfilehash: 81005ceac6bfa3c258a147f3fbef168e95c302cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174753"
---
# <span data-ttu-id="2606c-101">Reset-AzWebAppPublishingProfile</span><span class="sxs-lookup"><span data-stu-id="2606c-101">Reset-AzWebAppPublishingProfile</span></span>

## <span data-ttu-id="2606c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2606c-102">SYNOPSIS</span></span>

## <span data-ttu-id="2606c-103">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2606c-103">SYNTAX</span></span>

### <span data-ttu-id="2606c-104">S1</span><span class="sxs-lookup"><span data-stu-id="2606c-104">S1</span></span>
```
Reset-AzWebAppPublishingProfile [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2606c-105">S2</span><span class="sxs-lookup"><span data-stu-id="2606c-105">S2</span></span>
```
Reset-AzWebAppPublishingProfile [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2606c-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2606c-106">DESCRIPTION</span></span>
<span data-ttu-id="2606c-107">Das **Cmdlet "Reset-AzWebAppPublishingProfile"** setzt das Veröffentlichungsprofil für die angegebene Web App zurück.</span><span class="sxs-lookup"><span data-stu-id="2606c-107">The **Reset-AzWebAppPublishingProfile** cmdlet resets the publishing profile for the specified Web App.</span></span>

## <span data-ttu-id="2606c-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2606c-108">EXAMPLES</span></span>

### <span data-ttu-id="2606c-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2606c-109">Example 1</span></span>

<span data-ttu-id="2606c-110">Im folgenden Beispiel wird das Veröffentlichungsprofil für die Web App-IpRule zurückgesetzt, die der Ressourcengruppe "MyResourceGroup" zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="2606c-110">The following example resets the publishing profile for the Web App IpRule associated with the resource group MyResourceGroup.</span></span>

```powershell <!-- Aladdin Generated Example --> 
Reset-AzWebAppPublishingProfile -Name IpRule -ResourceGroupName MyResourceGroup
```

## <span data-ttu-id="2606c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2606c-111">PARAMETERS</span></span>

### <span data-ttu-id="2606c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2606c-112">-DefaultProfile</span></span>
<span data-ttu-id="2606c-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2606c-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2606c-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2606c-114">-Name</span></span>
<span data-ttu-id="2606c-115">WebApp Name</span><span class="sxs-lookup"><span data-stu-id="2606c-115">WebApp Name</span></span>

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

### <span data-ttu-id="2606c-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2606c-116">-ResourceGroupName</span></span>
<span data-ttu-id="2606c-117">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="2606c-117">Resource Group Name</span></span>

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

### <span data-ttu-id="2606c-118">-WebApp</span><span class="sxs-lookup"><span data-stu-id="2606c-118">-WebApp</span></span>
<span data-ttu-id="2606c-119">WebApp-Objekt</span><span class="sxs-lookup"><span data-stu-id="2606c-119">WebApp Object</span></span>

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

### <span data-ttu-id="2606c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2606c-120">CommonParameters</span></span>
<span data-ttu-id="2606c-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2606c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2606c-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2606c-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2606c-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2606c-123">INPUTS</span></span>

### <span data-ttu-id="2606c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2606c-124">System.String</span></span>

### <span data-ttu-id="2606c-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="2606c-125">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="2606c-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2606c-126">OUTPUTS</span></span>

### <span data-ttu-id="2606c-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2606c-127">System.String</span></span>

## <span data-ttu-id="2606c-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2606c-128">NOTES</span></span>

## <span data-ttu-id="2606c-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2606c-129">RELATED LINKS</span></span>
