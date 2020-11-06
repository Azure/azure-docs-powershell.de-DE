---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreFirewallRule.md
ms.openlocfilehash: 9d0b360e7284086b1cfadcba6ad17c47c22b6cb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478485"
---
# <span data-ttu-id="8a701-101">Remove-AzureRmDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8a701-101">Remove-AzureRmDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="8a701-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a701-102">SYNOPSIS</span></span>
<span data-ttu-id="8a701-103">Entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8a701-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a701-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a701-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8a701-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a701-105">DESCRIPTION</span></span>
<span data-ttu-id="8a701-106">Das Cmdlet **Remove-AzureRmDataLakeStoreFirewallRule** entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8a701-106">The **Remove-AzureRmDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8a701-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a701-107">EXAMPLES</span></span>

### <span data-ttu-id="8a701-108">Beispiel 1: Entfernen einer Firewall-Regel von einem Konto</span><span class="sxs-lookup"><span data-stu-id="8a701-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzureRmDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="8a701-109">Entfernt die Firewall-Regel "MyFirewallRule" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8a701-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="8a701-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a701-110">PARAMETERS</span></span>

### <span data-ttu-id="8a701-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8a701-111">-Account</span></span>
<span data-ttu-id="8a701-112">Das Data Lake Store-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="8a701-112">The Data Lake Store account to update the firewall rule in</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a701-113">-DefaultProfile</span></span>
<span data-ttu-id="8a701-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8a701-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8a701-115">-Name</span></span>
<span data-ttu-id="8a701-116">Der Name der Firewall-Regel, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a701-116">The name of the firewall rule to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a701-117">-PassThru</span></span>
<span data-ttu-id="8a701-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="8a701-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a701-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a701-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem die Firewall-Regel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a701-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a701-121">-Confirm</span></span>
<span data-ttu-id="8a701-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a701-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a701-123">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a701-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a701-124">CommonParameters</span></span>
<span data-ttu-id="8a701-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a701-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a701-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a701-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a701-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a701-127">INPUTS</span></span>

### <span data-ttu-id="8a701-128">Keine</span><span class="sxs-lookup"><span data-stu-id="8a701-128">None</span></span>
<span data-ttu-id="8a701-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8a701-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a701-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a701-130">OUTPUTS</span></span>

### <span data-ttu-id="8a701-131">bool</span><span class="sxs-lookup"><span data-stu-id="8a701-131">bool</span></span>
<span data-ttu-id="8a701-132">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a701-132">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="8a701-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a701-133">NOTES</span></span>

## <span data-ttu-id="8a701-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a701-134">RELATED LINKS</span></span>

