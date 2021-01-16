---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/new-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/New-AzMapsAccount.md
ms.openlocfilehash: 1e6358972e547e6a5fab54072396c3ad6fc7f418
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98298979"
---
# <span data-ttu-id="99ac1-101">New-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="99ac1-101">New-AzMapsAccount</span></span>

## <span data-ttu-id="99ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="99ac1-103">Erstellt ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="99ac1-103">Creates an Azure Maps account.</span></span>

## <span data-ttu-id="99ac1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99ac1-104">SYNTAX</span></span>

```
New-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String> [-Tag <Hashtable[]>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99ac1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="99ac1-106">Das New-AzMapsAccount erstellt ein Azure -Karten-Konto mit der angegebenen SKU.</span><span class="sxs-lookup"><span data-stu-id="99ac1-106">The New-AzMapsAccount cmdlet creates an Azure Maps account with the specified SKU.</span></span>

## <span data-ttu-id="99ac1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="99ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="99ac1-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="99ac1-108">Example 1</span></span>
```powershell
PS C:\> New-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="99ac1-109">Erstellt ein neues Azure -Karten-Konto mit dem Namen "MyAccount" in der Ressourcengruppe "MyResourceGroup" mit der SKU S0 und einem Tag.</span><span class="sxs-lookup"><span data-stu-id="99ac1-109">Creates a new Azure Maps account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="99ac1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99ac1-110">PARAMETERS</span></span>

### <span data-ttu-id="99ac1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99ac1-111">-DefaultProfile</span></span>
<span data-ttu-id="99ac1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99ac1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99ac1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="99ac1-113">-Force</span></span>
<span data-ttu-id="99ac1-114">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="99ac1-114">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ac1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="99ac1-115">-Name</span></span>
<span data-ttu-id="99ac1-116">Kartenkontoname.</span><span class="sxs-lookup"><span data-stu-id="99ac1-116">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99ac1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99ac1-117">-ResourceGroupName</span></span>
<span data-ttu-id="99ac1-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="99ac1-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99ac1-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="99ac1-119">-SkuName</span></span>
<span data-ttu-id="99ac1-120">Kartenkonto-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="99ac1-120">Maps Account Sku Name.</span></span>

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

### <span data-ttu-id="99ac1-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="99ac1-121">-Tag</span></span>
<span data-ttu-id="99ac1-122">Karten-Kontotags.</span><span class="sxs-lookup"><span data-stu-id="99ac1-122">Maps Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99ac1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="99ac1-123">-Confirm</span></span>
<span data-ttu-id="99ac1-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="99ac1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99ac1-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="99ac1-125">-WhatIf</span></span>
<span data-ttu-id="99ac1-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99ac1-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99ac1-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99ac1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99ac1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99ac1-128">CommonParameters</span></span>
<span data-ttu-id="99ac1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99ac1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99ac1-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99ac1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99ac1-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="99ac1-131">INPUTS</span></span>

### <span data-ttu-id="99ac1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="99ac1-132">System.String</span></span>

## <span data-ttu-id="99ac1-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="99ac1-133">OUTPUTS</span></span>

### <span data-ttu-id="99ac1-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="99ac1-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="99ac1-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="99ac1-135">NOTES</span></span>

## <span data-ttu-id="99ac1-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="99ac1-136">RELATED LINKS</span></span>
