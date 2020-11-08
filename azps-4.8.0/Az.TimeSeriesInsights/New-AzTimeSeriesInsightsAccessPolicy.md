---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173650"
---
# <span data-ttu-id="667b8-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="667b8-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="667b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="667b8-102">SYNOPSIS</span></span>
<span data-ttu-id="667b8-103">Erstellen oder Aktualisieren einer Zugriffsrichtlinie in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="667b8-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="667b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="667b8-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="667b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="667b8-105">DESCRIPTION</span></span>
<span data-ttu-id="667b8-106">Erstellen oder Aktualisieren einer Zugriffsrichtlinie in der angegebenen Umgebung</span><span class="sxs-lookup"><span data-stu-id="667b8-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="667b8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="667b8-107">EXAMPLES</span></span>

### <span data-ttu-id="667b8-108">Beispiel 1: Erstellen einer Zugriffsrichtlinie für eine bestimmte Umgebung</span><span class="sxs-lookup"><span data-stu-id="667b8-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="667b8-109">Mit diesem Befehl wird eine Zugriffsrichtlinie für eine bestimmte Umgebung erstellt.</span><span class="sxs-lookup"><span data-stu-id="667b8-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="667b8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="667b8-110">PARAMETERS</span></span>

### <span data-ttu-id="667b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="667b8-111">-DefaultProfile</span></span>
<span data-ttu-id="667b8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="667b8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-113">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="667b8-113">-Description</span></span>
<span data-ttu-id="667b8-114">Eine Beschreibung der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="667b8-114">An description of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-115">-Umgebungsname</span><span class="sxs-lookup"><span data-stu-id="667b8-115">-EnvironmentName</span></span>
<span data-ttu-id="667b8-116">Der Name der Zeitreihen Einblicke-Umgebung, die der angegebenen Ressourcengruppe zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="667b8-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="667b8-117">-Name</span><span class="sxs-lookup"><span data-stu-id="667b8-117">-Name</span></span>
<span data-ttu-id="667b8-118">Der Name der Zugriffsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="667b8-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="667b8-119">-PrincipalObjectId</span></span>
<span data-ttu-id="667b8-120">Die ObjectID des Prinzipals in Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="667b8-120">The objectId of the principal in Azure Active Directory.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="667b8-121">-ResourceGroupName</span></span>
<span data-ttu-id="667b8-122">Der Name einer Azure-Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="667b8-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="667b8-123">-Role</span><span class="sxs-lookup"><span data-stu-id="667b8-123">-Role</span></span>
<span data-ttu-id="667b8-124">Die Liste der Rollen, die dem Prinzipal in der Umgebung zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="667b8-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-125">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="667b8-125">-SubscriptionId</span></span>
<span data-ttu-id="667b8-126">Azure-Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="667b8-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="667b8-127">-Confirm</span></span>
<span data-ttu-id="667b8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="667b8-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="667b8-129">-WhatIf</span></span>
<span data-ttu-id="667b8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="667b8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="667b8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="667b8-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="667b8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="667b8-132">CommonParameters</span></span>
<span data-ttu-id="667b8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="667b8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="667b8-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="667b8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="667b8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="667b8-135">INPUTS</span></span>

## <span data-ttu-id="667b8-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="667b8-136">OUTPUTS</span></span>

### <span data-ttu-id="667b8-137">Microsoft. Azure. PowerShell. Cmdlets. TimeSeriesInsights. Models. Api20200515. IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="667b8-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="667b8-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="667b8-138">NOTES</span></span>

<span data-ttu-id="667b8-139">Aliase</span><span class="sxs-lookup"><span data-stu-id="667b8-139">ALIASES</span></span>

## <span data-ttu-id="667b8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="667b8-140">RELATED LINKS</span></span>

