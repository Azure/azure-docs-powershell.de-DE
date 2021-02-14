---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174609"
---
# <span data-ttu-id="04f9a-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04f9a-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="04f9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f9a-102">SYNOPSIS</span></span>
<span data-ttu-id="04f9a-103">Fügt einem Data Lake Analytics-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="04f9a-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="04f9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="04f9a-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f9a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="04f9a-105">DESCRIPTION</span></span>
<span data-ttu-id="04f9a-106">Das **Cmdlet "Add-AzDataLakeAnalyticsFirewallRule"** fügt einem Azure Data Lake Analytics-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="04f9a-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="04f9a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="04f9a-107">EXAMPLES</span></span>

### <span data-ttu-id="04f9a-108">Beispiel 1: Hinzufügen einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="04f9a-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="04f9a-109">Mit diesem Befehl wird die Firewallregel namens "Meine Firewallregel" aus dem Konto "ContosoAdlAcct" dem IP-Bereich hinzufügt: 127.0.0.1 bis 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="04f9a-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="04f9a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04f9a-110">PARAMETERS</span></span>

### <span data-ttu-id="04f9a-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="04f9a-111">-Account</span></span>
<span data-ttu-id="04f9a-112">Das Data Lake Analytics-Konto, dem die Firewallregel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="04f9a-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="04f9a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f9a-113">-DefaultProfile</span></span>
<span data-ttu-id="04f9a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="04f9a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04f9a-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="04f9a-115">-EndIpAddress</span></span>
<span data-ttu-id="04f9a-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="04f9a-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f9a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="04f9a-117">-Name</span></span>
<span data-ttu-id="04f9a-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="04f9a-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="04f9a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04f9a-119">-ResourceGroupName</span></span>
<span data-ttu-id="04f9a-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="04f9a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="04f9a-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="04f9a-121">-StartIpAddress</span></span>
<span data-ttu-id="04f9a-122">Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="04f9a-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f9a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04f9a-123">-Confirm</span></span>
<span data-ttu-id="04f9a-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04f9a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f9a-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="04f9a-125">-WhatIf</span></span>
<span data-ttu-id="04f9a-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04f9a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f9a-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04f9a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f9a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f9a-128">CommonParameters</span></span>
<span data-ttu-id="04f9a-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04f9a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f9a-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04f9a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f9a-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="04f9a-131">INPUTS</span></span>

### <span data-ttu-id="04f9a-132">System.String</span><span class="sxs-lookup"><span data-stu-id="04f9a-132">System.String</span></span>

## <span data-ttu-id="04f9a-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="04f9a-133">OUTPUTS</span></span>

### <span data-ttu-id="04f9a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="04f9a-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="04f9a-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="04f9a-135">NOTES</span></span>

## <span data-ttu-id="04f9a-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="04f9a-136">RELATED LINKS</span></span>
