---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010176"
---
# <span data-ttu-id="e7805-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e7805-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="e7805-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e7805-102">SYNOPSIS</span></span>
<span data-ttu-id="e7805-103">Gibt eine Liste von Datenbanken zurück, die im Besitz dieses Clusters sind und von einem anderen Cluster gefolgt sind.</span><span class="sxs-lookup"><span data-stu-id="e7805-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e7805-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7805-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e7805-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e7805-105">DESCRIPTION</span></span>
<span data-ttu-id="e7805-106">Gibt eine Liste von Datenbanken zurück, die im Besitz dieses Clusters sind und von einem anderen Cluster gefolgt sind.</span><span class="sxs-lookup"><span data-stu-id="e7805-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e7805-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e7805-107">EXAMPLES</span></span>

### <span data-ttu-id="e7805-108">Beispiel 1: Auflisten aller folgenden Datenbanken</span><span class="sxs-lookup"><span data-stu-id="e7805-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="e7805-109">Der obige Befehl listet alle Datenbanken auf, die im Besitz dieses Clusters sind und von einem anderen Cluster gefolgt sind.</span><span class="sxs-lookup"><span data-stu-id="e7805-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e7805-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7805-110">PARAMETERS</span></span>

### <span data-ttu-id="e7805-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="e7805-111">-ClusterName</span></span>
<span data-ttu-id="e7805-112">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="e7805-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e7805-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7805-113">-DefaultProfile</span></span>
<span data-ttu-id="e7805-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e7805-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7805-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7805-115">-ResourceGroupName</span></span>
<span data-ttu-id="e7805-116">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="e7805-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e7805-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="e7805-117">-SubscriptionId</span></span>
<span data-ttu-id="e7805-118">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7805-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7805-119">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="e7805-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e7805-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e7805-120">-Confirm</span></span>
<span data-ttu-id="e7805-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e7805-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7805-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7805-122">-WhatIf</span></span>
<span data-ttu-id="e7805-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e7805-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7805-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e7805-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7805-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7805-125">CommonParameters</span></span>
<span data-ttu-id="e7805-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7805-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7805-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7805-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7805-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e7805-128">INPUTS</span></span>

## <span data-ttu-id="e7805-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e7805-129">OUTPUTS</span></span>

### <span data-ttu-id="e7805-130">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="e7805-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="e7805-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e7805-131">NOTES</span></span>

<span data-ttu-id="e7805-132">Aliase</span><span class="sxs-lookup"><span data-stu-id="e7805-132">ALIASES</span></span>

## <span data-ttu-id="e7805-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e7805-133">RELATED LINKS</span></span>

