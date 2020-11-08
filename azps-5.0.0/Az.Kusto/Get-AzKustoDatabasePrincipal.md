---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustodatabaseprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoDatabasePrincipal.md
ms.openlocfilehash: c9b25327d170d05a4c2ad97b3cb7ce7626fbfec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179218"
---
# <span data-ttu-id="24efa-101">Get-AzKustoDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="24efa-101">Get-AzKustoDatabasePrincipal</span></span>

## <span data-ttu-id="24efa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24efa-102">SYNOPSIS</span></span>
<span data-ttu-id="24efa-103">Gibt eine Liste von Datenbankprinzipalen des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="24efa-103">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="24efa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24efa-104">SYNTAX</span></span>

```
Get-AzKustoDatabasePrincipal -ClusterName <String> -DatabaseName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="24efa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24efa-105">DESCRIPTION</span></span>
<span data-ttu-id="24efa-106">Gibt eine Liste von Datenbankprinzipalen des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="24efa-106">Returns a list of database principals of the given Kusto cluster and database.</span></span>

## <span data-ttu-id="24efa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24efa-107">EXAMPLES</span></span>

### <span data-ttu-id="24efa-108">Beispiel 1: Liste der Datenbankprinzipale des angegebenen Kusto-Clusters und der angegebenen Datenbank</span><span class="sxs-lookup"><span data-stu-id="24efa-108">Example 1: List of database principals of the given Kusto cluster and database</span></span>
```powershell
PS C:\> Get-AzKustoDatabasePrincipal -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase

AppId Email                   Fqn                                                                               Name        Role  TenantName Type
----- -----                   ---                                                                               ----        ----  ---------- ----
      someuser@microsoft.com  aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Some User   Admin Microsoft  User
      otheruser@microsoft.com aaduser=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx;xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx Other User  Admin Microsoft  User
```

<span data-ttu-id="24efa-109">Der obige Befehl gibt eine Liste von Datenbankprinzipalen des angegebenen Kusto-Clusters und der angegebenen Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="24efa-109">The above command returns a list of database principals of the given Kusto cluster and database</span></span>

## <span data-ttu-id="24efa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="24efa-110">PARAMETERS</span></span>

### <span data-ttu-id="24efa-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="24efa-111">-ClusterName</span></span>
<span data-ttu-id="24efa-112">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="24efa-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="24efa-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="24efa-113">-DatabaseName</span></span>
<span data-ttu-id="24efa-114">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="24efa-114">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="24efa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24efa-115">-DefaultProfile</span></span>
<span data-ttu-id="24efa-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24efa-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24efa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24efa-117">-ResourceGroupName</span></span>
<span data-ttu-id="24efa-118">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="24efa-118">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="24efa-119">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="24efa-119">-SubscriptionId</span></span>
<span data-ttu-id="24efa-120">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="24efa-120">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24efa-121">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="24efa-121">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24efa-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="24efa-122">-Confirm</span></span>
<span data-ttu-id="24efa-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="24efa-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24efa-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24efa-124">-WhatIf</span></span>
<span data-ttu-id="24efa-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="24efa-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24efa-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="24efa-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24efa-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24efa-127">CommonParameters</span></span>
<span data-ttu-id="24efa-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24efa-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24efa-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24efa-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24efa-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24efa-130">INPUTS</span></span>

## <span data-ttu-id="24efa-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24efa-131">OUTPUTS</span></span>

### <span data-ttu-id="24efa-132">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabasePrincipal</span><span class="sxs-lookup"><span data-stu-id="24efa-132">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipal</span></span>

## <span data-ttu-id="24efa-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="24efa-133">NOTES</span></span>

<span data-ttu-id="24efa-134">Aliase</span><span class="sxs-lookup"><span data-stu-id="24efa-134">ALIASES</span></span>

## <span data-ttu-id="24efa-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24efa-135">RELATED LINKS</span></span>

