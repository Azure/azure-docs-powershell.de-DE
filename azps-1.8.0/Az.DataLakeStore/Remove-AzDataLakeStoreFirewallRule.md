---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e4764fff543666d677689a029f0fb5b3089a99bb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820164"
---
# <span data-ttu-id="8b0db-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8b0db-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="8b0db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8b0db-102">SYNOPSIS</span></span>
<span data-ttu-id="8b0db-103">Entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8b0db-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8b0db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b0db-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8b0db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8b0db-105">DESCRIPTION</span></span>
<span data-ttu-id="8b0db-106">Das Cmdlet **Remove-AzDataLakeStoreFirewallRule** entfernt die angegebene Firewall-Regel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8b0db-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8b0db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8b0db-107">EXAMPLES</span></span>

### <span data-ttu-id="8b0db-108">Beispiel 1: Entfernen einer Firewall-Regel von einem Konto</span><span class="sxs-lookup"><span data-stu-id="8b0db-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="8b0db-109">Entfernt die Firewall-Regel "MyFirewallRule" aus dem Konto "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="8b0db-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="8b0db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b0db-110">PARAMETERS</span></span>

### <span data-ttu-id="8b0db-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8b0db-111">-Account</span></span>
<span data-ttu-id="8b0db-112">Das Data Lake Store-Konto zum Aktualisieren der Firewall-Regel in</span><span class="sxs-lookup"><span data-stu-id="8b0db-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="8b0db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b0db-113">-DefaultProfile</span></span>
<span data-ttu-id="8b0db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8b0db-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b0db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8b0db-115">-Name</span></span>
<span data-ttu-id="8b0db-116">Der Name der Firewall-Regel, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b0db-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="8b0db-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b0db-117">-PassThru</span></span>
<span data-ttu-id="8b0db-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="8b0db-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b0db-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b0db-119">-ResourceGroupName</span></span>
<span data-ttu-id="8b0db-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem die Firewall-Regel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8b0db-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="8b0db-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8b0db-121">-Confirm</span></span>
<span data-ttu-id="8b0db-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8b0db-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b0db-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b0db-123">-WhatIf</span></span>
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

### <span data-ttu-id="8b0db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b0db-124">CommonParameters</span></span>
<span data-ttu-id="8b0db-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b0db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b0db-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b0db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b0db-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8b0db-127">INPUTS</span></span>

### <span data-ttu-id="8b0db-128">System. String</span><span class="sxs-lookup"><span data-stu-id="8b0db-128">System.String</span></span>

### <span data-ttu-id="8b0db-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="8b0db-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8b0db-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8b0db-130">OUTPUTS</span></span>

### <span data-ttu-id="8b0db-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b0db-131">System.Boolean</span></span>

## <span data-ttu-id="8b0db-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="8b0db-132">NOTES</span></span>

## <span data-ttu-id="8b0db-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8b0db-133">RELATED LINKS</span></span>
