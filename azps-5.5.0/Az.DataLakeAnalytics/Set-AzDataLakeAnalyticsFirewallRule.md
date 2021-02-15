---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161972"
---
# <span data-ttu-id="e5dff-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5dff-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e5dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5dff-102">SYNOPSIS</span></span>
<span data-ttu-id="e5dff-103">Aktualisiert eine Firewallregel in einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="e5dff-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="e5dff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5dff-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5dff-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5dff-105">DESCRIPTION</span></span>
<span data-ttu-id="e5dff-106">Das **Cmdlet Set-AzDataLakeAnalyticsFirewallRule** aktualisiert eine Firewallregel in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="e5dff-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="e5dff-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e5dff-107">EXAMPLES</span></span>

### <span data-ttu-id="e5dff-108">Beispiel 1: Aktualisieren einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="e5dff-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="e5dff-109">Mit diesem Befehl wird die Firewallregel namens "Meine Firewallregel" im Konto "ContosoAdlAcct" so aktualisiert, dass der neue IP-Bereich gilt: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="e5dff-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="e5dff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5dff-110">PARAMETERS</span></span>

### <span data-ttu-id="e5dff-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e5dff-111">-Account</span></span>
<span data-ttu-id="e5dff-112">Das Data Lake Analytics-Konto, um die Firewallregel in</span><span class="sxs-lookup"><span data-stu-id="e5dff-112">The Data Lake Analytics account to update the firewall rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5dff-113">-DefaultProfile</span></span>
<span data-ttu-id="e5dff-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e5dff-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5dff-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="e5dff-115">-EndIpAddress</span></span>
<span data-ttu-id="e5dff-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="e5dff-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dff-117">-Name</span><span class="sxs-lookup"><span data-stu-id="e5dff-117">-Name</span></span>
<span data-ttu-id="e5dff-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="e5dff-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dff-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5dff-119">-ResourceGroupName</span></span>
<span data-ttu-id="e5dff-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e5dff-120">Name of resource group under which want to retrieve the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dff-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="e5dff-121">-StartIpAddress</span></span>
<span data-ttu-id="e5dff-122">Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="e5dff-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5dff-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5dff-123">-Confirm</span></span>
<span data-ttu-id="e5dff-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e5dff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5dff-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e5dff-125">-WhatIf</span></span>
<span data-ttu-id="e5dff-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e5dff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5dff-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e5dff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5dff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5dff-128">CommonParameters</span></span>
<span data-ttu-id="e5dff-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5dff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5dff-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5dff-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5dff-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e5dff-131">INPUTS</span></span>

### <span data-ttu-id="e5dff-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e5dff-132">System.String</span></span>

## <span data-ttu-id="e5dff-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e5dff-133">OUTPUTS</span></span>

### <span data-ttu-id="e5dff-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e5dff-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="e5dff-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e5dff-135">NOTES</span></span>

## <span data-ttu-id="e5dff-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e5dff-136">RELATED LINKS</span></span>
