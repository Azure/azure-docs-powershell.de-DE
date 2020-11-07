---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: ecb6088b3ca257967faff49b47a7ec2f3c2bf7bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651638"
---
# <span data-ttu-id="8f980-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f980-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8f980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f980-102">SYNOPSIS</span></span>
<span data-ttu-id="8f980-103">Fügt eine Firewallregel zu einem Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="8f980-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8f980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f980-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f980-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f980-105">DESCRIPTION</span></span>
<span data-ttu-id="8f980-106">Das Cmdlet **Add-AzDataLakeAnalyticsFirewallRule** fügt eine Firewallregel zu einem Azure Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="8f980-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8f980-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f980-107">EXAMPLES</span></span>

### <span data-ttu-id="8f980-108">Beispiel 1: Hinzufügen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="8f980-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="8f980-109">Mit diesem Befehl wird die Firewallregel mit dem Namen "meine Firewall-Regel" aus dem Konto "ContosoAdlAcct" mit dem IP-Bereich hinzugefügt: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="8f980-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="8f980-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f980-110">PARAMETERS</span></span>

### <span data-ttu-id="8f980-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8f980-111">-Account</span></span>
<span data-ttu-id="8f980-112">Das Data Lake Analytics-Konto, dem Sie die Firewallregel hinzufügen möchten</span><span class="sxs-lookup"><span data-stu-id="8f980-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="8f980-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f980-113">-DefaultProfile</span></span>
<span data-ttu-id="8f980-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f980-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f980-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="8f980-115">-EndIpAddress</span></span>
<span data-ttu-id="8f980-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="8f980-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="8f980-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8f980-117">-Name</span></span>
<span data-ttu-id="8f980-118">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="8f980-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="8f980-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f980-119">-ResourceGroupName</span></span>
<span data-ttu-id="8f980-120">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f980-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="8f980-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="8f980-121">-StartIpAddress</span></span>
<span data-ttu-id="8f980-122">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="8f980-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="8f980-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f980-123">-Confirm</span></span>
<span data-ttu-id="8f980-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f980-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f980-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f980-125">-WhatIf</span></span>
<span data-ttu-id="8f980-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f980-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f980-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f980-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f980-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f980-128">CommonParameters</span></span>
<span data-ttu-id="8f980-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f980-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f980-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f980-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f980-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f980-131">INPUTS</span></span>

### <span data-ttu-id="8f980-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8f980-132">System.String</span></span>

## <span data-ttu-id="8f980-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f980-133">OUTPUTS</span></span>

### <span data-ttu-id="8f980-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f980-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8f980-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f980-135">NOTES</span></span>

## <span data-ttu-id="8f980-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f980-136">RELATED LINKS</span></span>
