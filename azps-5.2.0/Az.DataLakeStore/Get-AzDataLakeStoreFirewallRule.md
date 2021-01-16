---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298568"
---
# <span data-ttu-id="2448b-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2448b-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="2448b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2448b-102">SYNOPSIS</span></span>
<span data-ttu-id="2448b-103">Ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="2448b-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="2448b-104">Wenn keine Firewallregel angegeben ist, werden alle Firewallregeln für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2448b-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="2448b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2448b-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2448b-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2448b-106">DESCRIPTION</span></span>
<span data-ttu-id="2448b-107">Das Get-AzDataLakeStoreFirewallRule-Cmdlet ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="2448b-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="2448b-108">Wenn keine Firewallregel angegeben ist, werden alle Firewallregeln für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="2448b-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="2448b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2448b-109">EXAMPLES</span></span>

### <span data-ttu-id="2448b-110">Beispiel 1: Abrufen einer bestimmten Firewallregel</span><span class="sxs-lookup"><span data-stu-id="2448b-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="2448b-111">Gibt die Firewallregel mit dem Namen "MyFirewallRule" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="2448b-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="2448b-112">Beispiel 2: Auflisten aller Firewallregeln in einem Konto</span><span class="sxs-lookup"><span data-stu-id="2448b-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="2448b-113">Gibt alle Firewallregeln im Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="2448b-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="2448b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2448b-114">PARAMETERS</span></span>

### <span data-ttu-id="2448b-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="2448b-115">-Account</span></span>
<span data-ttu-id="2448b-116">Das Data Lake Store-Konto, aus dem die Firewallregel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2448b-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="2448b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2448b-117">-DefaultProfile</span></span>
<span data-ttu-id="2448b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="2448b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2448b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="2448b-119">-Name</span></span>
<span data-ttu-id="2448b-120">Der Name der Firewallregel, die abgerufen werden soll</span><span class="sxs-lookup"><span data-stu-id="2448b-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="2448b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2448b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2448b-122">Name der Ressourcengruppe, unter der die angegebene Firewallregel des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="2448b-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="2448b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2448b-123">CommonParameters</span></span>
<span data-ttu-id="2448b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2448b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2448b-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2448b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2448b-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2448b-126">INPUTS</span></span>

### <span data-ttu-id="2448b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="2448b-127">System.String</span></span>

## <span data-ttu-id="2448b-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2448b-128">OUTPUTS</span></span>

### <span data-ttu-id="2448b-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2448b-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="2448b-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2448b-130">NOTES</span></span>

## <span data-ttu-id="2448b-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2448b-131">RELATED LINKS</span></span>
