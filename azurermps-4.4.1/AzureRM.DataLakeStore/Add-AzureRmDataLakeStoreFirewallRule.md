---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: C6FD4734-720C-4C8C-9B58-EDB331DD6415
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 45784bdcb684c1bd98ef1891042ad3ff6a172381
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663964"
---
# <span data-ttu-id="44205-101">Add-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44205-101">Add-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="44205-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="44205-102">SYNOPSIS</span></span>
<span data-ttu-id="44205-103">Fügt dem angegebenen Data Lake Store-Konto eine Firewallregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="44205-103">Adds a firewall rule to the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="44205-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="44205-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44205-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44205-105">DESCRIPTION</span></span>
<span data-ttu-id="44205-106">Mit dem Cmdlet **Add-AzureRmDataLakeStoreFirewallRule** wird dem angegebenen Data Lake Store-Konto eine Firewallregel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="44205-106">The **Add-AzureRmDataLakeStoreFirewallRule** cmdlet adds a firewall rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="44205-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="44205-107">EXAMPLES</span></span>

### <span data-ttu-id="44205-108">Beispiel 1: Hinzufügen einer neuen Firewallregel zu einem Data Lake Store-Konto</span><span class="sxs-lookup"><span data-stu-id="44205-108">Example 1: Add a new firewall rule to a Data Lake Store account</span></span>
```
PS C:\> Add-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="44205-109">Dadurch wird eine neue Firewall-Regel mit dem Namen "myrule" im Konto "ContosoADL" mit einem IP-Bereich von 127.0.0.1-127.0.0.2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="44205-109">This creates a new firewall rule called "MyRule" in account "ContosoADL" with an IP range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="44205-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="44205-110">PARAMETERS</span></span>

### <span data-ttu-id="44205-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="44205-111">-Account</span></span>
<span data-ttu-id="44205-112">Das Data Lake Store-Konto zum Hinzufügen der Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="44205-112">The Data Lake Store account to add the firewall rule to</span></span>

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

### <span data-ttu-id="44205-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="44205-113">-EndIpAddress</span></span>
<span data-ttu-id="44205-114">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="44205-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="44205-115">-Name</span><span class="sxs-lookup"><span data-stu-id="44205-115">-Name</span></span>
<span data-ttu-id="44205-116">Der Name der Firewall-Regel, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44205-116">The name of the firewall rule to add.</span></span>

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

### <span data-ttu-id="44205-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44205-117">-ResourceGroupName</span></span>
<span data-ttu-id="44205-118">Der Name der Ressourcengruppe, unter der sich das Konto befindet, dem die Firewallregel hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44205-118">Name of resource group under which the account to add the firewall rule is.</span></span>

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

### <span data-ttu-id="44205-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="44205-119">-StartIpAddress</span></span>
<span data-ttu-id="44205-120">Der Anfang des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="44205-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="44205-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="44205-121">-Confirm</span></span>
<span data-ttu-id="44205-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44205-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44205-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44205-123">-WhatIf</span></span>
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

### <span data-ttu-id="44205-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44205-124">-DefaultProfile</span></span>
<span data-ttu-id="44205-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="44205-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="44205-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44205-126">CommonParameters</span></span>
<span data-ttu-id="44205-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44205-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44205-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44205-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44205-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="44205-129">INPUTS</span></span>

## <span data-ttu-id="44205-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="44205-130">OUTPUTS</span></span>

### <span data-ttu-id="44205-131">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="44205-131">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="44205-132">Die Firewallregel, die hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="44205-132">The firewall rule that was added.</span></span>

## <span data-ttu-id="44205-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="44205-133">NOTES</span></span>

## <span data-ttu-id="44205-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="44205-134">RELATED LINKS</span></span>

