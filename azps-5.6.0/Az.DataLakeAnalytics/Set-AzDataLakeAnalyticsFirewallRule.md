---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 9fbb2064a7b7869af450ad267f73c6dc2e2b9a9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947931"
---
# <span data-ttu-id="ffd05-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffd05-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ffd05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffd05-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd05-103">Aktualisiert eine Firewallregel in einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="ffd05-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="ffd05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffd05-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffd05-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffd05-105">DESCRIPTION</span></span>
<span data-ttu-id="ffd05-106">Das **Cmdlet Set-AzDataLakeAnalyticsFirewallRule** aktualisiert eine Firewallregel in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="ffd05-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ffd05-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffd05-107">EXAMPLES</span></span>

### <span data-ttu-id="ffd05-108">Beispiel 1: Aktualisieren einer Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ffd05-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="ffd05-109">Mit diesem Befehl wird die Firewallregel mit dem Namen "meine Firewallregel" im Konto "ContosoAdlAcct" aktualisiert, um den neuen IP-Bereich zu verwenden: 127.0.0.1 - 127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="ffd05-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="ffd05-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ffd05-110">PARAMETERS</span></span>

### <span data-ttu-id="ffd05-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="ffd05-111">-Account</span></span>
<span data-ttu-id="ffd05-112">Das Data Lake Analytics-Konto zum Aktualisieren der Firewallregel in</span><span class="sxs-lookup"><span data-stu-id="ffd05-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="ffd05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd05-113">-DefaultProfile</span></span>
<span data-ttu-id="ffd05-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ffd05-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ffd05-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffd05-115">-EndIpAddress</span></span>
<span data-ttu-id="ffd05-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ffd05-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ffd05-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ffd05-117">-Name</span></span>
<span data-ttu-id="ffd05-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="ffd05-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ffd05-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd05-119">-ResourceGroupName</span></span>
<span data-ttu-id="ffd05-120">Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ffd05-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="ffd05-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ffd05-121">-StartIpAddress</span></span>
<span data-ttu-id="ffd05-122">Der Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="ffd05-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ffd05-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ffd05-123">-Confirm</span></span>
<span data-ttu-id="ffd05-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ffd05-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd05-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd05-125">-WhatIf</span></span>
<span data-ttu-id="ffd05-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ffd05-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd05-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ffd05-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd05-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd05-128">CommonParameters</span></span>
<span data-ttu-id="ffd05-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd05-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd05-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd05-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd05-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffd05-131">INPUTS</span></span>

### <span data-ttu-id="ffd05-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ffd05-132">System.String</span></span>

## <span data-ttu-id="ffd05-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffd05-133">OUTPUTS</span></span>

### <span data-ttu-id="ffd05-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ffd05-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ffd05-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ffd05-135">NOTES</span></span>

## <span data-ttu-id="ffd05-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ffd05-136">RELATED LINKS</span></span>
