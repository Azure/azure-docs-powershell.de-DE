---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: 3380835b4ca8e51c8ba0952ef3ef4bd973fadea3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918848"
---
# <span data-ttu-id="2b4b3-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="2b4b3-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="2b4b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4b3-103">Gibt eine Liste der Datenbankprinzipale des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="2b4b3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b4b3-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b4b3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2b4b3-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4b3-106">Gibt eine Liste der Datenbankprinzipale des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="2b4b3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2b4b3-107">EXAMPLES</span></span>

### <span data-ttu-id="2b4b3-108">Beispiel 1: Liste der Datenbankprinzipale des angegebenen Kusto-Clusters und der angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="2b4b3-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="2b4b3-109">Der obige Befehl gibt eine Liste der Datenbankprinzipale des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="2b4b3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2b4b3-110">PARAMETERS</span></span>

### <span data-ttu-id="2b4b3-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2b4b3-111">-ClusterName</span></span>
<span data-ttu-id="2b4b3-112">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="2b4b3-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b4b3-113">-DatabaseName</span></span>
<span data-ttu-id="2b4b3-114">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="2b4b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4b3-115">-DefaultProfile</span></span>
<span data-ttu-id="2b4b3-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b4b3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4b3-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b4b3-118">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="2b4b3-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b4b3-119">-SubscriptionId</span></span>
<span data-ttu-id="2b4b3-120">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b4b3-121">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2b4b3-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2b4b3-122">-Confirm</span></span>
<span data-ttu-id="2b4b3-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4b3-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4b3-124">-WhatIf</span></span>
<span data-ttu-id="2b4b3-125">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4b3-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4b3-127">CommonParameters</span></span>
<span data-ttu-id="2b4b3-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b4b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4b3-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b4b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4b3-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2b4b3-130">INPUTS</span></span>

## <span data-ttu-id="2b4b3-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2b4b3-131">OUTPUTS</span></span>

### <span data-ttu-id="2b4b3-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="2b4b3-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipal</span></span>

## <span data-ttu-id="2b4b3-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2b4b3-133">NOTES</span></span>

<span data-ttu-id="2b4b3-134">ALIASE</span><span class="sxs-lookup"><span data-stu-id="2b4b3-134">ALIASES</span></span>

## <span data-ttu-id="2b4b3-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2b4b3-135">RELATED LINKS</span></span>

