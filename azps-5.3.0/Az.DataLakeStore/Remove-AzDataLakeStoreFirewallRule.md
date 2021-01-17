---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6C7A7E1A-87A2-4F0D-9091-413C111F47F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: e583379f9541c056943081b804a84ecd7bee7bf5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458056"
---
# <span data-ttu-id="10598-101">Remove-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="10598-101">Remove-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="10598-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10598-102">SYNOPSIS</span></span>
<span data-ttu-id="10598-103">Entfernt die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10598-103">Removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="10598-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="10598-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10598-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="10598-105">DESCRIPTION</span></span>
<span data-ttu-id="10598-106">Das **Cmdlet "Remove-AzDataLakeStoreFirewallRule"** entfernt die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="10598-106">The **Remove-AzDataLakeStoreFirewallRule** cmdlet removes the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="10598-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="10598-107">EXAMPLES</span></span>

### <span data-ttu-id="10598-108">Beispiel 1: Entfernen einer Firewallregel aus einem Konto</span><span class="sxs-lookup"><span data-stu-id="10598-108">Example 1: Remove a firewall rule from an account</span></span>
```
PS C:\> Remove-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="10598-109">Entfernt die Firewallregel "MyFirewallRule" aus dem Konto "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="10598-109">Removes firewall rule "MyFirewallRule" from account "ContosoADL"</span></span>

## <span data-ttu-id="10598-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10598-110">PARAMETERS</span></span>

### <span data-ttu-id="10598-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="10598-111">-Account</span></span>
<span data-ttu-id="10598-112">Das Data Lake Store-Konto, um die Firewallregel in</span><span class="sxs-lookup"><span data-stu-id="10598-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="10598-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10598-113">-DefaultProfile</span></span>
<span data-ttu-id="10598-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="10598-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10598-115">-Name</span><span class="sxs-lookup"><span data-stu-id="10598-115">-Name</span></span>
<span data-ttu-id="10598-116">Der Name der zu löschende Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="10598-116">The name of the firewall rule to delete.</span></span>

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

### <span data-ttu-id="10598-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10598-117">-PassThru</span></span>
<span data-ttu-id="10598-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="10598-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="10598-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10598-119">-ResourceGroupName</span></span>
<span data-ttu-id="10598-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, aus dem die Firewallregel entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="10598-120">Specifies the name of the resource group that contains the account to remove the firewall rule from.</span></span>

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

### <span data-ttu-id="10598-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10598-121">-Confirm</span></span>
<span data-ttu-id="10598-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="10598-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10598-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="10598-123">-WhatIf</span></span>
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

### <span data-ttu-id="10598-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10598-124">CommonParameters</span></span>
<span data-ttu-id="10598-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10598-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10598-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10598-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10598-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="10598-127">INPUTS</span></span>

### <span data-ttu-id="10598-128">System.String</span><span class="sxs-lookup"><span data-stu-id="10598-128">System.String</span></span>

### <span data-ttu-id="10598-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10598-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10598-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="10598-130">OUTPUTS</span></span>

### <span data-ttu-id="10598-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10598-131">System.Boolean</span></span>

## <span data-ttu-id="10598-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="10598-132">NOTES</span></span>

## <span data-ttu-id="10598-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="10598-133">RELATED LINKS</span></span>
