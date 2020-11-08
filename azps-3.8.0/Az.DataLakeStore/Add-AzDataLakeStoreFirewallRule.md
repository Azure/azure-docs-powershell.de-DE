---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: a13125695ab5f4c57ab2e7013d64fff376643076
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995224"
---
# <span data-ttu-id="7e864-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e864-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7e864-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e864-102">SYNOPSIS</span></span>
<span data-ttu-id="7e864-103">Fügt dem angegebenen Data Lake Store-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="7e864-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="7e864-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e864-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e864-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e864-105">DESCRIPTION</span></span>
<span data-ttu-id="7e864-106">Mit dem Cmdlet **Add-AzDataLakeStoreFirewallRule** wird dem angegebenen Data Lake Store-Konto eine Firewallregel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7e864-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="7e864-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e864-107">EXAMPLES</span></span>

### <span data-ttu-id="7e864-108">Beispiel 1: Hinzufügen einer neuen Firewallregel zu einem Data Lake Store-Konto</span><span class="sxs-lookup"><span data-stu-id="7e864-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="7e864-109">Dadurch wird eine neue Firewall-Regel mit dem Namen "myrule" im Konto "ContosoADL" mit einem IP-Bereich von 127.0.0.1-127.0.0.2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e864-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="7e864-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e864-110">PARAMETERS</span></span>

### <span data-ttu-id="7e864-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="7e864-111">-Account</span></span>
<span data-ttu-id="7e864-112">Das Data Lake Store-Konto zum Hinzufügen der Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="7e864-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="7e864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e864-113">-DefaultProfile</span></span>
<span data-ttu-id="7e864-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7e864-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e864-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e864-115">-EndIpAddress</span></span>
<span data-ttu-id="7e864-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="7e864-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7e864-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7e864-117">-Name</span></span>
<span data-ttu-id="7e864-118">Der Name der Firewall-Regel, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e864-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="7e864-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e864-119">-ResourceGroupName</span></span>
<span data-ttu-id="7e864-120">Der Name der Ressourcengruppe, unter der sich das Konto befindet, dem die Firewallregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e864-120">Name of resource group under which the account to add the firewall rule is.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e864-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="7e864-121">-StartIpAddress</span></span>
<span data-ttu-id="7e864-122">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="7e864-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="7e864-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7e864-123">-Confirm</span></span>
<span data-ttu-id="7e864-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7e864-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e864-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e864-125">-WhatIf</span></span>
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

### <span data-ttu-id="7e864-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e864-126">CommonParameters</span></span>
<span data-ttu-id="7e864-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e864-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e864-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e864-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e864-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e864-129">INPUTS</span></span>

### <span data-ttu-id="7e864-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7e864-130">System.String</span></span>

## <span data-ttu-id="7e864-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e864-131">OUTPUTS</span></span>

### <span data-ttu-id="7e864-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="7e864-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="7e864-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e864-133">NOTES</span></span>

## <span data-ttu-id="7e864-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e864-134">RELATED LINKS</span></span>
