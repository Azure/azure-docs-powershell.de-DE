---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 8f83b199aae030bc0ff8cb8290bb6b273e0c8cff
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459115"
---
# <span data-ttu-id="f62e4-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f62e4-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="f62e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f62e4-102">SYNOPSIS</span></span>
<span data-ttu-id="f62e4-103">Gibt eine Liste der Datenbankprinzipale des angegebenen Cluster und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f62e4-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f62e4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f62e4-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f62e4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f62e4-105">DESCRIPTION</span></span>
<span data-ttu-id="f62e4-106">Gibt eine Liste der Datenbankprinzipale des angegebenen Cluster und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="f62e4-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="f62e4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f62e4-107">EXAMPLES</span></span>

### <span data-ttu-id="f62e4-108">Beispiel 1: Liste der Datenbankprinzipale für den angegebenen Cluster und die angegebene Datenbank in Kusto</span><span class="sxs-lookup"><span data-stu-id="f62e4-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="f62e4-109">Der oben aufgeführte Befehl gibt eine Liste der Datenbankprinzipale des angegebenen Cluster- und Datenbankprojekts "Kusto" zurück.</span><span class="sxs-lookup"><span data-stu-id="f62e4-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="f62e4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f62e4-110">PARAMETERS</span></span>

### <span data-ttu-id="f62e4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="f62e4-111">-ClusterName</span></span>
<span data-ttu-id="f62e4-112">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="f62e4-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e4-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f62e4-113">-DatabaseName</span></span>
<span data-ttu-id="f62e4-114">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="f62e4-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62e4-115">-DefaultProfile</span></span>
<span data-ttu-id="f62e4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f62e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f62e4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62e4-117">-ResourceGroupName</span></span>
<span data-ttu-id="f62e4-118">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="f62e4-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="f62e4-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f62e4-119">-SubscriptionId</span></span>
<span data-ttu-id="f62e4-120">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f62e4-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f62e4-121">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="f62e4-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f62e4-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f62e4-122">-Confirm</span></span>
<span data-ttu-id="f62e4-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f62e4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f62e4-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f62e4-124">-WhatIf</span></span>
<span data-ttu-id="f62e4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f62e4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f62e4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f62e4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f62e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62e4-127">CommonParameters</span></span>
<span data-ttu-id="f62e4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f62e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62e4-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f62e4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62e4-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f62e4-130">INPUTS</span></span>

## <span data-ttu-id="f62e4-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f62e4-131">OUTPUTS</span></span>

### <span data-ttu-id="f62e4-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="f62e4-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="f62e4-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f62e4-133">NOTES</span></span>

<span data-ttu-id="f62e4-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="f62e4-134">ALIASES</span></span>

## <span data-ttu-id="f62e4-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f62e4-135">RELATED LINKS</span></span>

