---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370724"
---
# <span data-ttu-id="4dafd-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="4dafd-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="4dafd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4dafd-102">SYNOPSIS</span></span>
<span data-ttu-id="4dafd-103">Löscht ein Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="4dafd-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="4dafd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4dafd-104">SYNTAX</span></span>

### <span data-ttu-id="4dafd-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4dafd-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dafd-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dafd-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4dafd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4dafd-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dafd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4dafd-108">DESCRIPTION</span></span>
<span data-ttu-id="4dafd-109">Das Remove-AzMapsAccount cmdlet löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="4dafd-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="4dafd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4dafd-110">EXAMPLES</span></span>

### <span data-ttu-id="4dafd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4dafd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4dafd-112">Löscht das Konto "MeinAccount" aus der Ressourcengruppe "MyResourceGroup".</span><span class="sxs-lookup"><span data-stu-id="4dafd-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="4dafd-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4dafd-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="4dafd-114">Löscht das angegebene Azure Maps-Konto.</span><span class="sxs-lookup"><span data-stu-id="4dafd-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="4dafd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4dafd-115">PARAMETERS</span></span>

### <span data-ttu-id="4dafd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dafd-116">-DefaultProfile</span></span>
<span data-ttu-id="4dafd-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dafd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dafd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dafd-118">-InputObject</span></span>
<span data-ttu-id="4dafd-119">Maps Account piped from Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="4dafd-119">Maps Account piped from Get-AzMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4dafd-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4dafd-120">-Name</span></span>
<span data-ttu-id="4dafd-121">Kartenkontoname.</span><span class="sxs-lookup"><span data-stu-id="4dafd-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dafd-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dafd-122">-PassThru</span></span>
<span data-ttu-id="4dafd-123">Gibt zurück, ob das angegebene Konto erfolgreich gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="4dafd-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="4dafd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4dafd-124">-ResourceGroupName</span></span>
<span data-ttu-id="4dafd-125">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="4dafd-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dafd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dafd-126">-ResourceId</span></span>
<span data-ttu-id="4dafd-127">Karten "Account ResourceId".</span><span class="sxs-lookup"><span data-stu-id="4dafd-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4dafd-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dafd-128">-Confirm</span></span>
<span data-ttu-id="4dafd-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4dafd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dafd-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4dafd-130">-WhatIf</span></span>
<span data-ttu-id="4dafd-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dafd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dafd-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4dafd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dafd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dafd-133">CommonParameters</span></span>
<span data-ttu-id="4dafd-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dafd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dafd-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dafd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dafd-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4dafd-136">INPUTS</span></span>

### <span data-ttu-id="4dafd-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4dafd-137">System.String</span></span>

### <span data-ttu-id="4dafd-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="4dafd-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="4dafd-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4dafd-139">OUTPUTS</span></span>

### <span data-ttu-id="4dafd-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4dafd-140">System.Boolean</span></span>

## <span data-ttu-id="4dafd-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4dafd-141">NOTES</span></span>

## <span data-ttu-id="4dafd-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4dafd-142">RELATED LINKS</span></span>
