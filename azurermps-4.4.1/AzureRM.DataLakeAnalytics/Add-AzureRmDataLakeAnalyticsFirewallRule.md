---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479297"
---
# <span data-ttu-id="92a04-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92a04-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="92a04-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92a04-102">SYNOPSIS</span></span>
<span data-ttu-id="92a04-103">Fügt eine Firewallregel zu einem Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="92a04-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92a04-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92a04-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92a04-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92a04-105">DESCRIPTION</span></span>
<span data-ttu-id="92a04-106">Das Cmdlet **Add-AzureRmDataLakeAnalyticsFirewallRule** fügt eine Firewallregel zu einem Azure Data Lake Analytics-Konto hinzu.</span><span class="sxs-lookup"><span data-stu-id="92a04-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="92a04-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92a04-107">EXAMPLES</span></span>

### <span data-ttu-id="92a04-108">Beispiel 1: Hinzufügen einer Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="92a04-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="92a04-109">Mit diesem Befehl wird die Firewallregel mit dem Namen "meine Firewall-Regel" aus dem Konto "ContosoAdlAcct" mit dem IP-Bereich hinzugefügt: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="92a04-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="92a04-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92a04-110">PARAMETERS</span></span>

### <span data-ttu-id="92a04-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="92a04-111">-Account</span></span>
<span data-ttu-id="92a04-112">Das Data Lake Analytics-Konto, dem Sie die Firewallregel hinzufügen möchten</span><span class="sxs-lookup"><span data-stu-id="92a04-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="92a04-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="92a04-113">-EndIpAddress</span></span>
<span data-ttu-id="92a04-114">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="92a04-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="92a04-115">-Name</span><span class="sxs-lookup"><span data-stu-id="92a04-115">-Name</span></span>
<span data-ttu-id="92a04-116">Der Name der Firewall-Regel.</span><span class="sxs-lookup"><span data-stu-id="92a04-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="92a04-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92a04-117">-ResourceGroupName</span></span>
<span data-ttu-id="92a04-118">Der Name der Ressourcengruppe, unter der das Konto abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="92a04-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="92a04-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="92a04-119">-StartIpAddress</span></span>
<span data-ttu-id="92a04-120">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="92a04-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="92a04-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92a04-121">-Confirm</span></span>
<span data-ttu-id="92a04-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92a04-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92a04-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92a04-123">-WhatIf</span></span>
<span data-ttu-id="92a04-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92a04-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92a04-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92a04-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92a04-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92a04-126">-DefaultProfile</span></span>
<span data-ttu-id="92a04-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92a04-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92a04-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92a04-128">CommonParameters</span></span>
<span data-ttu-id="92a04-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92a04-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92a04-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92a04-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92a04-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92a04-131">INPUTS</span></span>

### <span data-ttu-id="92a04-132">System. String</span><span class="sxs-lookup"><span data-stu-id="92a04-132">System.String</span></span>

## <span data-ttu-id="92a04-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92a04-133">OUTPUTS</span></span>

### <span data-ttu-id="92a04-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="92a04-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="92a04-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="92a04-135">NOTES</span></span>

## <span data-ttu-id="92a04-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92a04-136">RELATED LINKS</span></span>

