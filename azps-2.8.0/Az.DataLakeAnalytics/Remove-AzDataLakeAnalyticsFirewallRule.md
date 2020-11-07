---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 6d179a4cc5814c45925802f606480927a3ed3af0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651601"
---
# <span data-ttu-id="236aa-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="236aa-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="236aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="236aa-102">SYNOPSIS</span></span>
<span data-ttu-id="236aa-103">Entfernt eine Firewall-Regel aus einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="236aa-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="236aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="236aa-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="236aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="236aa-105">DESCRIPTION</span></span>
<span data-ttu-id="236aa-106">Das Cmdlet **Remove-AzDataLakeAnalyticsFirewallRule** entfernt eine Firewallregel aus einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="236aa-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="236aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="236aa-107">EXAMPLES</span></span>

### <span data-ttu-id="236aa-108">Beispiel 1: Entfernen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="236aa-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="236aa-109">Dieser Befehl entfernt die Firewallregel mit dem Namen "meine Firewall-Regel" aus dem Konto "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="236aa-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="236aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="236aa-110">PARAMETERS</span></span>

### <span data-ttu-id="236aa-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="236aa-111">-Account</span></span>
<span data-ttu-id="236aa-112">Das Data Lake Analytics-Konto, aus dem die Firewallregel entfernt werden soll</span><span class="sxs-lookup"><span data-stu-id="236aa-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="236aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="236aa-113">-DefaultProfile</span></span>
<span data-ttu-id="236aa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="236aa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="236aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="236aa-115">-Name</span></span>
<span data-ttu-id="236aa-116">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="236aa-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="236aa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="236aa-117">-PassThru</span></span>
<span data-ttu-id="236aa-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="236aa-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="236aa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="236aa-119">-ResourceGroupName</span></span>
<span data-ttu-id="236aa-120">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="236aa-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="236aa-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="236aa-121">-Confirm</span></span>
<span data-ttu-id="236aa-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="236aa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="236aa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="236aa-123">-WhatIf</span></span>
<span data-ttu-id="236aa-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="236aa-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="236aa-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="236aa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="236aa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="236aa-126">CommonParameters</span></span>
<span data-ttu-id="236aa-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="236aa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="236aa-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="236aa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="236aa-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="236aa-129">INPUTS</span></span>

### <span data-ttu-id="236aa-130">System. String</span><span class="sxs-lookup"><span data-stu-id="236aa-130">System.String</span></span>

### <span data-ttu-id="236aa-131">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="236aa-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="236aa-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="236aa-132">OUTPUTS</span></span>

### <span data-ttu-id="236aa-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="236aa-133">System.Boolean</span></span>

## <span data-ttu-id="236aa-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="236aa-134">NOTES</span></span>

## <span data-ttu-id="236aa-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="236aa-135">RELATED LINKS</span></span>
