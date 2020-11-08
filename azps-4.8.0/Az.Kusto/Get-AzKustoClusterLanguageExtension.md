---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterlanguageextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterLanguageExtension.md
ms.openlocfilehash: f33d644e9726d09f9f2314e74a6b5fb80b788952
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010175"
---
# <span data-ttu-id="c1584-101">Get-AzKustoClusterLanguageExtension</span><span class="sxs-lookup"><span data-stu-id="c1584-101">Get-AzKustoClusterLanguageExtension</span></span>

## <span data-ttu-id="c1584-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1584-102">SYNOPSIS</span></span>
<span data-ttu-id="c1584-103">Gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c1584-103">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c1584-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1584-104">SYNTAX</span></span>

```
Get-AzKustoClusterLanguageExtension -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1584-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1584-105">DESCRIPTION</span></span>
<span data-ttu-id="c1584-106">Gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c1584-106">Returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c1584-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1584-107">EXAMPLES</span></span>

### <span data-ttu-id="c1584-108">Beispiel 1: Auflisten aller Spracherweiterungen, die für einen Cluster eingerichtet wurden</span><span class="sxs-lookup"><span data-stu-id="c1584-108">Example 1: List all language extensions set for a cluster</span></span>
```powershell
PS C:\> Get-AzKustoClusterLanguageExtension -ResourceGroupName testrg -ClusterName testnewkustocluster

Name
----
R
PYTHON
```

<span data-ttu-id="c1584-109">Der obige Befehl gibt eine Liste der Spracherweiterungen zurück, die innerhalb von KQL-Abfragen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c1584-109">The above command returns a list of language extensions that can run within KQL queries.</span></span>

## <span data-ttu-id="c1584-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1584-110">PARAMETERS</span></span>

### <span data-ttu-id="c1584-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="c1584-111">-ClusterName</span></span>
<span data-ttu-id="c1584-112">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="c1584-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c1584-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1584-113">-DefaultProfile</span></span>
<span data-ttu-id="c1584-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1584-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1584-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1584-115">-ResourceGroupName</span></span>
<span data-ttu-id="c1584-116">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="c1584-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c1584-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c1584-117">-SubscriptionId</span></span>
<span data-ttu-id="c1584-118">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c1584-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c1584-119">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c1584-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c1584-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1584-120">-Confirm</span></span>
<span data-ttu-id="c1584-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1584-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1584-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1584-122">-WhatIf</span></span>
<span data-ttu-id="c1584-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1584-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1584-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1584-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1584-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1584-125">CommonParameters</span></span>
<span data-ttu-id="c1584-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1584-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1584-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1584-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1584-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1584-128">INPUTS</span></span>

## <span data-ttu-id="c1584-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1584-129">OUTPUTS</span></span>

### <span data-ttu-id="c1584-130">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. ILanguageExtension</span><span class="sxs-lookup"><span data-stu-id="c1584-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.ILanguageExtension</span></span>

## <span data-ttu-id="c1584-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1584-131">NOTES</span></span>

<span data-ttu-id="c1584-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="c1584-132">ALIASES</span></span>

## <span data-ttu-id="c1584-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1584-133">RELATED LINKS</span></span>

