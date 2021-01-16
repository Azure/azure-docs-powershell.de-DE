---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98299136"
---
# <span data-ttu-id="a5de9-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="a5de9-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="a5de9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5de9-102">SYNOPSIS</span></span>
<span data-ttu-id="a5de9-103">Gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a5de9-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="a5de9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5de9-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a5de9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5de9-105">DESCRIPTION</span></span>
<span data-ttu-id="a5de9-106">Gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a5de9-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="a5de9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5de9-107">EXAMPLES</span></span>

### <span data-ttu-id="a5de9-108">Beispiel 1: Auflisten aller für einen Cluster festgelegten Spracherweiterungen</span><span class="sxs-lookup"><span data-stu-id="a5de9-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="a5de9-109">Der oben aufgeführte Befehl gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="a5de9-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="a5de9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5de9-110">PARAMETERS</span></span>

### <span data-ttu-id="a5de9-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="a5de9-111">-ClusterName</span></span>
<span data-ttu-id="a5de9-112">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a5de9-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5de9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5de9-113">-DefaultProfile</span></span>
<span data-ttu-id="a5de9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5de9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5de9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5de9-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5de9-116">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="a5de9-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="a5de9-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5de9-117">-SubscriptionId</span></span>
<span data-ttu-id="a5de9-118">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a5de9-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a5de9-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="a5de9-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5de9-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5de9-120">-Confirm</span></span>
<span data-ttu-id="a5de9-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5de9-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5de9-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5de9-122">-WhatIf</span></span>
<span data-ttu-id="a5de9-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5de9-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5de9-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5de9-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5de9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5de9-125">CommonParameters</span></span>
<span data-ttu-id="a5de9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5de9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5de9-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5de9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5de9-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5de9-128">INPUTS</span></span>

## <span data-ttu-id="a5de9-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5de9-129">OUTPUTS</span></span>

### <span data-ttu-id="a5de9-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="a5de9-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="a5de9-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5de9-131">NOTES</span></span>

<span data-ttu-id="a5de9-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="a5de9-132">ALIASES</span></span>

## <span data-ttu-id="a5de9-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5de9-133">RELATED LINKS</span></span>

