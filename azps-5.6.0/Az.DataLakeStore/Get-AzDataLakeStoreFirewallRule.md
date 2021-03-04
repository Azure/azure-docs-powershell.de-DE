---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 580b5518e1fc0894a51920e781464258bef9e9cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925947"
---
# <span data-ttu-id="e1d84-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e1d84-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e1d84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1d84-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d84-103">Ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="e1d84-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e1d84-104">Wenn keine Firewallregel angegeben ist, werden alle Firewallregeln für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1d84-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="e1d84-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1d84-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1d84-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e1d84-106">DESCRIPTION</span></span>
<span data-ttu-id="e1d84-107">Das Get-AzDataLakeStoreFirewallRule-Cmdlet ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="e1d84-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="e1d84-108">Wenn keine Firewallregel angegeben ist, werden alle Firewallregeln für das Konto aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1d84-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="e1d84-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e1d84-109">EXAMPLES</span></span>

### <span data-ttu-id="e1d84-110">Beispiel 1: Abrufen einer bestimmten Firewallregel</span><span class="sxs-lookup"><span data-stu-id="e1d84-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="e1d84-111">Gibt die Firewallregel mit dem Namen "MyFirewallRule" vom Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="e1d84-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="e1d84-112">Beispiel 2: Auflisten aller Firewallregeln in einem Konto</span><span class="sxs-lookup"><span data-stu-id="e1d84-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="e1d84-113">Gibt alle Firewallregeln im Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="e1d84-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="e1d84-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e1d84-114">PARAMETERS</span></span>

### <span data-ttu-id="e1d84-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="e1d84-115">-Account</span></span>
<span data-ttu-id="e1d84-116">Das Data Lake Store-Konto, aus dem die Firewallregel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1d84-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="e1d84-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d84-117">-DefaultProfile</span></span>
<span data-ttu-id="e1d84-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e1d84-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1d84-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e1d84-119">-Name</span></span>
<span data-ttu-id="e1d84-120">Der Name der abzurufende Firewallregel</span><span class="sxs-lookup"><span data-stu-id="e1d84-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="e1d84-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d84-121">-ResourceGroupName</span></span>
<span data-ttu-id="e1d84-122">Name der Ressourcengruppe, unter der die angegebene Firewallregel des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e1d84-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="e1d84-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d84-123">CommonParameters</span></span>
<span data-ttu-id="e1d84-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d84-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d84-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d84-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d84-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e1d84-126">INPUTS</span></span>

### <span data-ttu-id="e1d84-127">System.String</span><span class="sxs-lookup"><span data-stu-id="e1d84-127">System.String</span></span>

## <span data-ttu-id="e1d84-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e1d84-128">OUTPUTS</span></span>

### <span data-ttu-id="e1d84-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="e1d84-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="e1d84-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e1d84-130">NOTES</span></span>

## <span data-ttu-id="e1d84-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e1d84-131">RELATED LINKS</span></span>
