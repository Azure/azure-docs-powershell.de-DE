---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 9983EA1E-2515-4F5D-8476-8D0EE9837E88
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 5c807c3d134768c7682b2216178eabd5a0771701
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458047"
---
# <span data-ttu-id="60dbe-101">Set-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="60dbe-101">Set-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="60dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="60dbe-103">Ändert die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="60dbe-103">Modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="60dbe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60dbe-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60dbe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60dbe-105">DESCRIPTION</span></span>
<span data-ttu-id="60dbe-106">Das **Cmdlet "Set-AzDataLakeStoreFirewallRule"** ändert die angegebene Firewallregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="60dbe-106">The **Set-AzDataLakeStoreFirewallRule** cmdlet modifies the specified firewall rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="60dbe-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60dbe-107">EXAMPLES</span></span>

### <span data-ttu-id="60dbe-108">Beispiel 1: Aktualisieren des Start- und End-IP-Bereichs für eine Firewallregel</span><span class="sxs-lookup"><span data-stu-id="60dbe-108">Example 1: Update the start and end IP range for a firewall rule</span></span>
```
PS C:\> Set-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule -StartIpAddress "127.0.0.1" -EndIpAddress "127.0.0.2"
```

<span data-ttu-id="60dbe-109">Aktualisiert die Firewallregel "MyFirewallRule" im Konto "ContosoADL" auf einen Bereich von 127.0.0.1 bis 127.0.0.2</span><span class="sxs-lookup"><span data-stu-id="60dbe-109">Updates the firewall rule "MyFirewallRule" in account "ContosoADL" to have a range of 127.0.0.1 - 127.0.0.2</span></span>

## <span data-ttu-id="60dbe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60dbe-110">PARAMETERS</span></span>

### <span data-ttu-id="60dbe-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="60dbe-111">-Account</span></span>
<span data-ttu-id="60dbe-112">Das Data Lake Store-Konto, um die Firewallregel in</span><span class="sxs-lookup"><span data-stu-id="60dbe-112">The Data Lake Store account to update the firewall rule in</span></span>

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

### <span data-ttu-id="60dbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60dbe-113">-DefaultProfile</span></span>
<span data-ttu-id="60dbe-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="60dbe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60dbe-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="60dbe-115">-EndIpAddress</span></span>
<span data-ttu-id="60dbe-116">Das Ende des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="60dbe-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="60dbe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="60dbe-117">-Name</span></span>
<span data-ttu-id="60dbe-118">Der Name der Firewallregel.</span><span class="sxs-lookup"><span data-stu-id="60dbe-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="60dbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60dbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="60dbe-120">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das die Firewallregel aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="60dbe-120">Specifies the name of the resource group that contains the account to update the firewall rule for.</span></span>

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

### <span data-ttu-id="60dbe-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="60dbe-121">-StartIpAddress</span></span>
<span data-ttu-id="60dbe-122">Start des gültigen IP-Bereichs für die Firewallregel</span><span class="sxs-lookup"><span data-stu-id="60dbe-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="60dbe-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60dbe-123">-Confirm</span></span>
<span data-ttu-id="60dbe-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60dbe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60dbe-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="60dbe-125">-WhatIf</span></span>
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

### <span data-ttu-id="60dbe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60dbe-126">CommonParameters</span></span>
<span data-ttu-id="60dbe-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60dbe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60dbe-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60dbe-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60dbe-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60dbe-129">INPUTS</span></span>

### <span data-ttu-id="60dbe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="60dbe-130">System.String</span></span>

## <span data-ttu-id="60dbe-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60dbe-131">OUTPUTS</span></span>

### <span data-ttu-id="60dbe-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="60dbe-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="60dbe-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60dbe-133">NOTES</span></span>

## <span data-ttu-id="60dbe-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60dbe-134">RELATED LINKS</span></span>
