---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 191b1ebc1f83387a9cf1ac59f6fb3f7a55f115ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477850"
---
# <span data-ttu-id="19584-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="19584-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="19584-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19584-102">SYNOPSIS</span></span>
<span data-ttu-id="19584-103">Ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="19584-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="19584-104">Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="19584-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19584-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19584-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19584-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19584-106">DESCRIPTION</span></span>
<span data-ttu-id="19584-107">Das Get-AzureRmDataLakeStoreFirewallRule-Cmdlet ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="19584-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="19584-108">Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="19584-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="19584-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19584-109">EXAMPLES</span></span>

### <span data-ttu-id="19584-110">Beispiel 1: Abrufen einer bestimmten Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="19584-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="19584-111">Gibt die Firewall-Regel mit dem Namen "MyFirewallRule" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="19584-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="19584-112">Beispiel 2: Auflisten aller Firewallregeln in einem Konto</span><span class="sxs-lookup"><span data-stu-id="19584-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="19584-113">Gibt alle Firewall-Regeln im Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="19584-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="19584-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="19584-114">PARAMETERS</span></span>

### <span data-ttu-id="19584-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="19584-115">-Account</span></span>
<span data-ttu-id="19584-116">Das Data Lake Store-Konto, aus dem die Firewall-Regel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="19584-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="19584-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19584-117">-DefaultProfile</span></span>
<span data-ttu-id="19584-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="19584-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19584-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19584-119">-Name</span></span>
<span data-ttu-id="19584-120">Der Name der Firewall-Regel, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="19584-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="19584-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19584-121">-ResourceGroupName</span></span>
<span data-ttu-id="19584-122">Der Name der Ressourcengruppe, unter der die angegebene Firewall-Regel des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="19584-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="19584-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19584-123">CommonParameters</span></span>
<span data-ttu-id="19584-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19584-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19584-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19584-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19584-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19584-126">INPUTS</span></span>

### <span data-ttu-id="19584-127">System. String</span><span class="sxs-lookup"><span data-stu-id="19584-127">System.String</span></span>

## <span data-ttu-id="19584-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19584-128">OUTPUTS</span></span>

### <span data-ttu-id="19584-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="19584-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="19584-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="19584-130">NOTES</span></span>

## <span data-ttu-id="19584-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19584-131">RELATED LINKS</span></span>
