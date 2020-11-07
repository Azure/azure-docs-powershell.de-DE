---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 8c7d936f8ea64534016286e97b34d36f41a72cf7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663962"
---
# <span data-ttu-id="1cad0-101">Get-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1cad0-101">Get-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="1cad0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1cad0-102">SYNOPSIS</span></span>
<span data-ttu-id="1cad0-103">Ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1cad0-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1cad0-104">Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1cad0-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1cad0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cad0-105">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cad0-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1cad0-106">DESCRIPTION</span></span>
<span data-ttu-id="1cad0-107">Das Get-AzureRmDataLakeStoreFirewallRule-Cmdlet ruft die angegebenen Firewallregeln im angegebenen Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="1cad0-107">The Get-AzureRmDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="1cad0-108">Wenn keine Firewall-Regel angegeben ist, werden alle Firewallregeln für das Konto aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1cad0-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="1cad0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1cad0-109">EXAMPLES</span></span>

### <span data-ttu-id="1cad0-110">Beispiel 1: Abrufen einer bestimmten Firewall-Regel</span><span class="sxs-lookup"><span data-stu-id="1cad0-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="1cad0-111">Gibt die Firewall-Regel mit dem Namen "MyFirewallRule" aus dem Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="1cad0-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="1cad0-112">Beispiel 2: Auflisten aller Firewallregeln in einem Konto</span><span class="sxs-lookup"><span data-stu-id="1cad0-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="1cad0-113">Gibt alle Firewall-Regeln im Konto "ContosoADL" zurück.</span><span class="sxs-lookup"><span data-stu-id="1cad0-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="1cad0-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cad0-114">PARAMETERS</span></span>

### <span data-ttu-id="1cad0-115">-Konto</span><span class="sxs-lookup"><span data-stu-id="1cad0-115">-Account</span></span>
<span data-ttu-id="1cad0-116">Das Data Lake Store-Konto, aus dem die Firewall-Regel abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cad0-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="1cad0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1cad0-117">-Name</span></span>
<span data-ttu-id="1cad0-118">Der Name der Firewall-Regel, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cad0-118">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="1cad0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cad0-119">-ResourceGroupName</span></span>
<span data-ttu-id="1cad0-120">Der Name der Ressourcengruppe, unter der die angegebene Firewall-Regel des angegebenen Kontos abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cad0-120">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="1cad0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cad0-121">-DefaultProfile</span></span>
<span data-ttu-id="1cad0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1cad0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1cad0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cad0-123">CommonParameters</span></span>
<span data-ttu-id="1cad0-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cad0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cad0-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cad0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cad0-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1cad0-126">INPUTS</span></span>

## <span data-ttu-id="1cad0-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1cad0-127">OUTPUTS</span></span>

### <span data-ttu-id="1cad0-128">DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="1cad0-128">DataLakeStoreFirewallRule</span></span>
<span data-ttu-id="1cad0-129">Die angegebene Firewall-Regel zum Abrufen</span><span class="sxs-lookup"><span data-stu-id="1cad0-129">The specified firewall rule to retrieve</span></span>

### <span data-ttu-id="1cad0-130">IList<DataLakeStoreFirewallRule></span><span class="sxs-lookup"><span data-stu-id="1cad0-130">IList<DataLakeStoreFirewallRule></span></span>
<span data-ttu-id="1cad0-131">Die Liste der Firewallregeln im angegebenen Konto.</span><span class="sxs-lookup"><span data-stu-id="1cad0-131">The list of firewall rules in the specified account.</span></span>

## <span data-ttu-id="1cad0-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="1cad0-132">NOTES</span></span>

## <span data-ttu-id="1cad0-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1cad0-133">RELATED LINKS</span></span>

