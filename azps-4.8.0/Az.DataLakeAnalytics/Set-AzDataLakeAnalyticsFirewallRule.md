---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175236"
---
# <span data-ttu-id="3eb98-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3eb98-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="3eb98-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3eb98-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb98-103">Aktualisiert eine Firewall-Regel in einem Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="3eb98-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="3eb98-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3eb98-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb98-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3eb98-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb98-106">Das Cmdlet " **Satz-AzDataLakeAnalyticsFirewallRule** " aktualisiert eine Firewallregel in einem Azure Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="3eb98-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3eb98-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3eb98-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb98-108">Beispiel 1: Aktualisieren einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="3eb98-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="3eb98-109">Dieser Befehl aktualisiert die Firewallregel mit dem Namen "meine Firewall-Regel" im Konto "ContosoAdlAcct", um den neuen IP-Bereich zu haben: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="3eb98-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="3eb98-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3eb98-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb98-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3eb98-111">-Account</span></span>
<span data-ttu-id="3eb98-112">Das Data Lake Analytics-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="3eb98-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="3eb98-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb98-113">-DefaultProfile</span></span>
<span data-ttu-id="3eb98-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3eb98-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eb98-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="3eb98-115">-EndIpAddress</span></span>
<span data-ttu-id="3eb98-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="3eb98-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3eb98-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3eb98-117">-Name</span></span>
<span data-ttu-id="3eb98-118">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="3eb98-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="3eb98-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb98-119">-ResourceGroupName</span></span>
<span data-ttu-id="3eb98-120">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eb98-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="3eb98-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="3eb98-121">-StartIpAddress</span></span>
<span data-ttu-id="3eb98-122">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="3eb98-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="3eb98-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3eb98-123">-Confirm</span></span>
<span data-ttu-id="3eb98-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3eb98-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb98-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb98-125">-WhatIf</span></span>
<span data-ttu-id="3eb98-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eb98-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb98-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3eb98-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb98-128">CommonParameters</span></span>
<span data-ttu-id="3eb98-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eb98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb98-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb98-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb98-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3eb98-131">INPUTS</span></span>

### <span data-ttu-id="3eb98-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3eb98-132">System.String</span></span>

## <span data-ttu-id="3eb98-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3eb98-133">OUTPUTS</span></span>

### <span data-ttu-id="3eb98-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="3eb98-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="3eb98-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="3eb98-135">NOTES</span></span>

## <span data-ttu-id="3eb98-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3eb98-136">RELATED LINKS</span></span>
