---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007847"
---
# <span data-ttu-id="733b6-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="733b6-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="733b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="733b6-102">SYNOPSIS</span></span>
<span data-ttu-id="733b6-103">Ruft eine Application Control VM/Server-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="733b6-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="733b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="733b6-104">SYNTAX</span></span>

### <span data-ttu-id="733b6-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="733b6-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="733b6-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="733b6-106">DESCRIPTION</span></span>
<span data-ttu-id="733b6-107">Steuerelemente für die Adaptive Anwendung werden automatisch vom Azure Security Center berechnet, verwenden Sie dieses Cmdlet, um eine VM/Server-Gruppe für die Anwendungssteuerung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="733b6-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="733b6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="733b6-108">EXAMPLES</span></span>

### <span data-ttu-id="733b6-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="733b6-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="733b6-110">Ruft eine Application Control VM/Server-Gruppe ab.</span><span class="sxs-lookup"><span data-stu-id="733b6-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="733b6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="733b6-111">PARAMETERS</span></span>

### <span data-ttu-id="733b6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="733b6-112">-DefaultProfile</span></span>
<span data-ttu-id="733b6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="733b6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="733b6-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="733b6-114">-AscLocation</span></span>
<span data-ttu-id="733b6-115">Der Speicherort, an dem ASC die Daten des Abonnements speichert.</span><span class="sxs-lookup"><span data-stu-id="733b6-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="733b6-116">kann von Get-Speicherorten abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="733b6-116">can be retrieved from Get locations.</span></span>

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

### <span data-ttu-id="733b6-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="733b6-117">-GroupName</span></span>
<span data-ttu-id="733b6-118">Name einer Application Control-VM/Server-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="733b6-118">Name of an application control VM/server group.</span></span>

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

### <span data-ttu-id="733b6-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="733b6-119">-SubscriptionId</span></span>
<span data-ttu-id="733b6-120">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="733b6-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="733b6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="733b6-121">CommonParameters</span></span>
<span data-ttu-id="733b6-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="733b6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="733b6-123">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="733b6-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="733b6-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="733b6-124">INPUTS</span></span>

### <span data-ttu-id="733b6-125">System. String</span><span class="sxs-lookup"><span data-stu-id="733b6-125">System.String</span></span>

## <span data-ttu-id="733b6-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="733b6-126">OUTPUTS</span></span>

### <span data-ttu-id="733b6-127">Microsoft. Azure. Commands. Security. Models. AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="733b6-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="733b6-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="733b6-128">NOTES</span></span>

## <span data-ttu-id="733b6-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="733b6-129">RELATED LINKS</span></span>