---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100162020"
---
# <span data-ttu-id="916de-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="916de-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="916de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="916de-102">SYNOPSIS</span></span>
<span data-ttu-id="916de-103">Entfernt eine Firewallregel aus einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="916de-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="916de-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="916de-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="916de-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="916de-105">DESCRIPTION</span></span>
<span data-ttu-id="916de-106">Das **Cmdlet "Remove-AzDataLakeAnalyticsFirewallRule"** entfernt eine Firewallregel aus einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="916de-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="916de-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="916de-107">EXAMPLES</span></span>

### <span data-ttu-id="916de-108">Beispiel 1: Entfernen einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="916de-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="916de-109">Mit diesem Befehl wird die Firewallregel mit dem Namen "Meine Firewallregel" aus dem Konto "ContosoAdlAcct" entfernt.</span><span class="sxs-lookup"><span data-stu-id="916de-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="916de-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="916de-110">PARAMETERS</span></span>

### <span data-ttu-id="916de-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="916de-111">-Account</span></span>
<span data-ttu-id="916de-112">Das Data Lake Analytics-Konto, aus dem die Firewallregel entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="916de-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="916de-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="916de-113">-DefaultProfile</span></span>
<span data-ttu-id="916de-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="916de-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="916de-115">-Name</span><span class="sxs-lookup"><span data-stu-id="916de-115">-Name</span></span>
<span data-ttu-id="916de-116">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="916de-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916de-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="916de-117">-PassThru</span></span>
<span data-ttu-id="916de-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden sollte, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="916de-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="916de-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="916de-119">-ResourceGroupName</span></span>
<span data-ttu-id="916de-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="916de-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="916de-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="916de-121">-Confirm</span></span>
<span data-ttu-id="916de-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="916de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="916de-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="916de-123">-WhatIf</span></span>
<span data-ttu-id="916de-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="916de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="916de-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="916de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="916de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="916de-126">CommonParameters</span></span>
<span data-ttu-id="916de-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="916de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="916de-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="916de-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="916de-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="916de-129">INPUTS</span></span>

### <span data-ttu-id="916de-130">System.String</span><span class="sxs-lookup"><span data-stu-id="916de-130">System.String</span></span>

### <span data-ttu-id="916de-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="916de-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="916de-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="916de-132">OUTPUTS</span></span>

### <span data-ttu-id="916de-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="916de-133">System.Boolean</span></span>

## <span data-ttu-id="916de-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="916de-134">NOTES</span></span>

## <span data-ttu-id="916de-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="916de-135">RELATED LINKS</span></span>
