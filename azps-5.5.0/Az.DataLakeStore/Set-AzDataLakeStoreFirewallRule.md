---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148132"
---
# <span data-ttu-id="a0047-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0047-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a0047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0047-102">SYNOPSIS</span></span>
<span data-ttu-id="a0047-103">Ändert die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0047-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a0047-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a0047-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0047-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a0047-105">DESCRIPTION</span></span>
<span data-ttu-id="a0047-106">Das **Cmdlet "Set-AzDataLakeStoreFirewallRule"** ändert die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a0047-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a0047-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a0047-107">EXAMPLES</span></span>

### <span data-ttu-id="a0047-108">Beispiel 1: Aktualisieren des Start- und End-IP-Bereichs für eine Firewallregel</span><span class="sxs-lookup"><span data-stu-id="a0047-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="a0047-109">Aktualisiert die Firewallregel "MyFirewallRule" im Konto "ContosoADL" auf einen Bereich von 127.0.0.1 bis 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="a0047-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="a0047-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a0047-110">PARAMETERS</span></span>

### <span data-ttu-id="a0047-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a0047-111">-Account</span></span>
<span data-ttu-id="a0047-112">Das Data Lake Store-Konto, um die Firewallregel in</span><span class="sxs-lookup"><span data-stu-id="a0047-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="a0047-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0047-113">-DefaultProfile</span></span>
<span data-ttu-id="a0047-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a0047-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0047-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0047-115">-EndIpAddress</span></span>
<span data-ttu-id="a0047-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="a0047-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0047-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a0047-117">-Name</span></span>
<span data-ttu-id="a0047-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="a0047-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="a0047-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0047-119">-ResourceGroupName</span></span>
<span data-ttu-id="a0047-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das die Firewallregel aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a0047-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0047-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="a0047-121">-StartIpAddress</span></span>
<span data-ttu-id="a0047-122">Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="a0047-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="a0047-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a0047-123">-Confirm</span></span>
<span data-ttu-id="a0047-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0047-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0047-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a0047-125">-WhatIf</span></span>
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

### <span data-ttu-id="a0047-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0047-126">CommonParameters</span></span>
<span data-ttu-id="a0047-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0047-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0047-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0047-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0047-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a0047-129">INPUTS</span></span>

### <span data-ttu-id="a0047-130">System.String</span><span class="sxs-lookup"><span data-stu-id="a0047-130">System.String</span></span>

## <span data-ttu-id="a0047-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a0047-131">OUTPUTS</span></span>

### <span data-ttu-id="a0047-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="a0047-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="a0047-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a0047-133">NOTES</span></span>

## <span data-ttu-id="a0047-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a0047-134">RELATED LINKS</span></span>
