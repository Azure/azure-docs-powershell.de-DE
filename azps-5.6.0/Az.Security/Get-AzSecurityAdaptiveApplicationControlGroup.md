---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: c23c04a5a9df3464bd84a2261435c744374cfb3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948480"
---
# <span data-ttu-id="31030-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="31030-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="31030-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31030-102">SYNOPSIS</span></span>
<span data-ttu-id="31030-103">Ruft eine VM/Server-Gruppe für anwendungssteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="31030-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="31030-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="31030-104">SYNTAX</span></span>

### <span data-ttu-id="31030-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="31030-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31030-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31030-106">DESCRIPTION</span></span>
<span data-ttu-id="31030-107">Adaptive Anwendungssteuerelemente werden automatisch vom Azure Security Center berechnet. Verwenden Sie dieses Cmdlet, um eine VM/Server-Gruppe für anwendungssteuerelemente zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="31030-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="31030-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="31030-108">EXAMPLES</span></span>

### <span data-ttu-id="31030-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="31030-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="31030-110">Ruft eine VM/Server-Gruppe für anwendungssteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="31030-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="31030-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="31030-111">PARAMETERS</span></span>

### <span data-ttu-id="31030-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31030-112">-DefaultProfile</span></span>
<span data-ttu-id="31030-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="31030-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31030-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="31030-114">-AscLocation</span></span>
<span data-ttu-id="31030-115">Der Speicherort, an dem ASC die Daten des Abonnements speichert.</span><span class="sxs-lookup"><span data-stu-id="31030-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="31030-116">kann aus Abrufen von Speicherorten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="31030-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31030-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="31030-117">-GroupName</span></span>
<span data-ttu-id="31030-118">Name einer Vm/Server-Gruppe für anwendungssteuerelemente.</span><span class="sxs-lookup"><span data-stu-id="31030-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31030-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31030-119">-SubscriptionId</span></span>
<span data-ttu-id="31030-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="31030-120">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="31030-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31030-121">CommonParameters</span></span>
<span data-ttu-id="31030-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31030-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31030-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31030-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31030-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="31030-124">INPUTS</span></span>

### <span data-ttu-id="31030-125">System.String</span><span class="sxs-lookup"><span data-stu-id="31030-125">System.String</span></span>

## <span data-ttu-id="31030-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="31030-126">OUTPUTS</span></span>

### <span data-ttu-id="31030-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="31030-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="31030-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="31030-128">NOTES</span></span>

## <span data-ttu-id="31030-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="31030-129">RELATED LINKS</span></span>