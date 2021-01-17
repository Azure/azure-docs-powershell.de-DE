---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472052"
---
# <span data-ttu-id="ab287-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="ab287-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="ab287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab287-102">SYNOPSIS</span></span>
<span data-ttu-id="ab287-103">Ruft eine Liste der VM/Server-Gruppen für die Anwendungssteuerung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ab287-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="ab287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ab287-104">SYNTAX</span></span>

### <span data-ttu-id="ab287-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="ab287-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ab287-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ab287-106">DESCRIPTION</span></span>
<span data-ttu-id="ab287-107">Steuerelemente für adaptive Anwendungen werden automatisch vom Azure Security Center berechnet. Verwenden Sie dieses Cmdlet, um eine Liste der Ressourcen für adaptive Anwendungssteuerelemente im Rahmen eines Abonnements zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ab287-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="ab287-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ab287-108">EXAMPLES</span></span>

### <span data-ttu-id="ab287-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ab287-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="ab287-110">Ruft eine Liste der VM/Server-Gruppen für die Anwendungssteuerung für das Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ab287-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="ab287-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab287-111">PARAMETERS</span></span>

### <span data-ttu-id="ab287-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab287-112">-DefaultProfile</span></span>
<span data-ttu-id="ab287-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ab287-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab287-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ab287-114">-SubscriptionId</span></span>
<span data-ttu-id="ab287-115">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="ab287-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="ab287-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="ab287-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="ab287-117">Schließen Sie die Richtlinienregeln ein.</span><span class="sxs-lookup"><span data-stu-id="ab287-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab287-118">-Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="ab287-118">-Summary</span></span>
<span data-ttu-id="ab287-119">Gibt die Ausgabe in einem zusammengefassten Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="ab287-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab287-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab287-120">CommonParameters</span></span>
<span data-ttu-id="ab287-121">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab287-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab287-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab287-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab287-123">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ab287-123">INPUTS</span></span>

### <span data-ttu-id="ab287-124">System.String</span><span class="sxs-lookup"><span data-stu-id="ab287-124">System.String</span></span>

### <span data-ttu-id="ab287-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ab287-125">System.Boolean</span></span>

## <span data-ttu-id="ab287-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ab287-126">OUTPUTS</span></span>

### <span data-ttu-id="ab287-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="ab287-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="ab287-128">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ab287-128">NOTES</span></span>

## <span data-ttu-id="ab287-129">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ab287-129">RELATED LINKS</span></span>
