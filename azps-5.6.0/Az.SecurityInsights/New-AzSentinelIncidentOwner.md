---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincidentowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentOwner.md
ms.openlocfilehash: b8981d40f3412dd77ca120cd80d29fb160915e8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918096"
---
# <span data-ttu-id="7c178-101">New-AzSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="7c178-101">New-AzSentinelIncidentOwner</span></span>

## <span data-ttu-id="7c178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c178-102">SYNOPSIS</span></span>
<span data-ttu-id="7c178-103">Erstellen Sie das Objekt "Vorfallbesitzer", um einen Vorfallbesitzer zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7c178-103">Create Incident Owner object to update an incident owner.</span></span>

## <span data-ttu-id="7c178-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c178-104">SYNTAX</span></span>

```
New-AzSentinelIncidentOwner -AssignedTo <String> -Email <String> -ObjectId <String> -UserPrincipalName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c178-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c178-105">DESCRIPTION</span></span>
<span data-ttu-id="7c178-106">Das **Cmdlet New-AzSentinelIncidentOwner** erstellt ein Incident Owner-Objekt im Arbeitsspeicher, um einen Vorfall zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7c178-106">The **New-AzSentinelIncidentOwner** cmdlet creates a Incident Owner object in memory to update an incident.</span></span>

## <span data-ttu-id="7c178-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c178-107">EXAMPLES</span></span>

### <span data-ttu-id="7c178-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c178-108">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $owner = New-AzSentinelIncidentOwner -AssignedTo "First Last" -Email "user@domain.com" -Objectid "userobjectId" -UserPrincipalName "user@domain.com"
PS C:\> $Incident.Owner = $owner
PS C:\> $Incident | Set-AzSentinelIncident
```

<span data-ttu-id="7c178-109">In diesem Beispiel wird ein **IncidentOwner erstellt** und ein Vorfall für den neuen Besitzer aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7c178-109">This example creates an **IncidentOwner** and updates an Incident to the new owner.</span></span>

## <span data-ttu-id="7c178-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c178-110">PARAMETERS</span></span>

### <span data-ttu-id="7c178-111">-AssignedTo</span><span class="sxs-lookup"><span data-stu-id="7c178-111">-AssignedTo</span></span>
<span data-ttu-id="7c178-112">Vorfallbesitzer – Zugewiesen an</span><span class="sxs-lookup"><span data-stu-id="7c178-112">Incident Owner - Assigned To</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c178-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c178-113">-DefaultProfile</span></span>
<span data-ttu-id="7c178-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c178-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c178-115">-E-Mail</span><span class="sxs-lookup"><span data-stu-id="7c178-115">-Email</span></span>
<span data-ttu-id="7c178-116">Vorfallbesitzer – E-Mail</span><span class="sxs-lookup"><span data-stu-id="7c178-116">Incident Owner - Email</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c178-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7c178-117">-ObjectId</span></span>
<span data-ttu-id="7c178-118">Vorfallbesitzer – ObjectId</span><span class="sxs-lookup"><span data-stu-id="7c178-118">Incident Owner - ObjectId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c178-119">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7c178-119">-UserPrincipalName</span></span>
<span data-ttu-id="7c178-120">Vorfallbesitzer – Name des Prinzipalbenutzers</span><span class="sxs-lookup"><span data-stu-id="7c178-120">Incident Owner - User Principal Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c178-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c178-121">CommonParameters</span></span>
<span data-ttu-id="7c178-122">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c178-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c178-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c178-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c178-124">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c178-124">INPUTS</span></span>

### <span data-ttu-id="7c178-125">Keine</span><span class="sxs-lookup"><span data-stu-id="7c178-125">None</span></span>
## <span data-ttu-id="7c178-126">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c178-126">OUTPUTS</span></span>

### <span data-ttu-id="7c178-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="7c178-127">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="7c178-128">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7c178-128">NOTES</span></span>

## <span data-ttu-id="7c178-129">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7c178-129">RELATED LINKS</span></span>
