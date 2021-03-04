---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 60a3363716bb4e93efa02cc63d3e83548c4944f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945179"
---
# <span data-ttu-id="c2ac9-101">Add-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c2ac9-101">Add-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="c2ac9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ac9-103">Fügt dem angegebenen Data Lake Store-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c2ac9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2ac9-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ac9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="c2ac9-106">Das **Add-AzDataLakeStoreFirewallRule-Cmdlet** fügt dem angegebenen Data Lake Store-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-106">The **Add-AzDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c2ac9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="c2ac9-108">Beispiel 1: Hinzufügen einer neuen Firewallregel zu einem Data Lake Store-Konto</span><span class="sxs-lookup"><span data-stu-id="c2ac9-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="c2ac9-109">Dadurch wird eine neue Firewallregel namens "MyRule" im Konto "ContosoADL" mit einem IP-Bereich von 127.0.0.1 - 127.0.0.2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="c2ac9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="c2ac9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="c2ac9-111">-Account</span></span>
<span data-ttu-id="c2ac9-112">Das Data Lake Store-Konto, dem die Firewallregel hinzugefügt werden soll</span><span class="sxs-lookup"><span data-stu-id="c2ac9-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="c2ac9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ac9-113">-DefaultProfile</span></span>
<span data-ttu-id="c2ac9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c2ac9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2ac9-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2ac9-115">-EndIpAddress</span></span>
<span data-ttu-id="c2ac9-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="c2ac9-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c2ac9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c2ac9-117">-Name</span></span>
<span data-ttu-id="c2ac9-118">Der Name der hinzuzufügende Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-118">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="c2ac9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2ac9-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2ac9-120">Name der Ressourcengruppe, unter der sich das Konto befindet, unter dem die Firewallregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-120">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="c2ac9-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c2ac9-121">-StartIpAddress</span></span>
<span data-ttu-id="c2ac9-122">Der Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="c2ac9-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c2ac9-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2ac9-123">-Confirm</span></span>
<span data-ttu-id="c2ac9-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ac9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ac9-125">-WhatIf</span></span>
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

### <span data-ttu-id="c2ac9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ac9-126">CommonParameters</span></span>
<span data-ttu-id="c2ac9-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ac9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ac9-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ac9-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ac9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2ac9-129">INPUTS</span></span>

### <span data-ttu-id="c2ac9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="c2ac9-130">System.String</span></span>

## <span data-ttu-id="c2ac9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2ac9-131">OUTPUTS</span></span>

### <span data-ttu-id="c2ac9-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c2ac9-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="c2ac9-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2ac9-133">NOTES</span></span>

## <span data-ttu-id="c2ac9-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2ac9-134">RELATED LINKS</span></span>
