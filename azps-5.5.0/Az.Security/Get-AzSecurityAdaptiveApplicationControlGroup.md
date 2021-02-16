---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158452"
---
# <span data-ttu-id="317d9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="317d9-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="317d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317d9-102">SYNOPSIS</span></span>
<span data-ttu-id="317d9-103">Ruft eine VM/Server-Gruppe für Anwendungssteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="317d9-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="317d9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="317d9-104">SYNTAX</span></span>

### <span data-ttu-id="317d9-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="317d9-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317d9-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="317d9-106">DESCRIPTION</span></span>
<span data-ttu-id="317d9-107">Steuerelemente für adaptive Anwendungen werden automatisch vom Azure Security Center berechnet. Verwenden Sie dieses Cmdlet, um eine VM/Server-Gruppe für das Anwendungssteuerelement zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="317d9-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="317d9-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="317d9-108">EXAMPLES</span></span>

### <span data-ttu-id="317d9-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="317d9-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="317d9-110">Ruft eine VM/Server-Gruppe für Anwendungssteuerelemente ab.</span><span class="sxs-lookup"><span data-stu-id="317d9-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="317d9-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="317d9-111">PARAMETERS</span></span>

### <span data-ttu-id="317d9-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317d9-112">-DefaultProfile</span></span>
<span data-ttu-id="317d9-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="317d9-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="317d9-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="317d9-114">-AscLocation</span></span>
<span data-ttu-id="317d9-115">Der Speicherort, an dem ASC die Daten des Abonnements speichert.</span><span class="sxs-lookup"><span data-stu-id="317d9-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="317d9-116">aus "Speicherorte abrufen" abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="317d9-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="317d9-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="317d9-117">-GroupName</span></span>
<span data-ttu-id="317d9-118">Name einer VM/Server-Gruppe für das Anwendungssteuerelement.</span><span class="sxs-lookup"><span data-stu-id="317d9-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="317d9-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="317d9-119">-SubscriptionId</span></span>
<span data-ttu-id="317d9-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="317d9-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="317d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317d9-121">CommonParameters</span></span>
<span data-ttu-id="317d9-122">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="317d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317d9-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317d9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317d9-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="317d9-124">INPUTS</span></span>

### <span data-ttu-id="317d9-125">System.String</span><span class="sxs-lookup"><span data-stu-id="317d9-125">System.String</span></span>

## <span data-ttu-id="317d9-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="317d9-126">OUTPUTS</span></span>

### <span data-ttu-id="317d9-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="317d9-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="317d9-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="317d9-128">NOTES</span></span>

## <span data-ttu-id="317d9-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="317d9-129">RELATED LINKS</span></span>