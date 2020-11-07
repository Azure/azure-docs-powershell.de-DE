---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 3041e69903eaac7a748aff52c83e2e994fae22f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93822915"
---
# <span data-ttu-id="8a3f4-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="8a3f4-101">Remove-AzBastion</span></span>

## <span data-ttu-id="8a3f4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="8a3f4-103">Entfernt eine Bastions Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="8a3f4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a3f4-104">SYNTAX</span></span>

### <span data-ttu-id="8a3f4-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a3f4-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a3f4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8a3f4-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a3f4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8a3f4-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a3f4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a3f4-108">DESCRIPTION</span></span>
<span data-ttu-id="8a3f4-109">Entfernt eine Bastions Ressource. Beispiel1 löscht die Bastion mithilfe der ResourceGroupName-und resourceName-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="8a3f4-110">Example2 löscht die Bastion mithilfe Ihres Objekts mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="8a3f4-111">Example3 löscht die Bastion mithilfe Ihres Objekts.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="8a3f4-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a3f4-112">EXAMPLES</span></span>

### <span data-ttu-id="8a3f4-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a3f4-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="8a3f4-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8a3f4-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="8a3f4-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8a3f4-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="8a3f4-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a3f4-116">PARAMETERS</span></span>

### <span data-ttu-id="8a3f4-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-117">-Confirm</span></span>
<span data-ttu-id="8a3f4-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a3f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a3f4-119">-DefaultProfile</span></span>
<span data-ttu-id="8a3f4-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8a3f4-121">-Force</span></span>
<span data-ttu-id="8a3f4-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-122">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a3f4-123">-InputObject</span></span>
<span data-ttu-id="8a3f4-124">Das zu löschende Bastion-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8a3f4-125">-Name</span></span>
<span data-ttu-id="8a3f4-126">Der Name der zu löschenden Bastion-Ressource.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a3f4-127">-PassThru</span></span>
<span data-ttu-id="8a3f4-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-128">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a3f4-129">-ResourceGroupName</span></span>
<span data-ttu-id="8a3f4-130">Der Ressourcengruppenname, in dem Bastion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8a3f4-131">-ResourceId</span></span>
<span data-ttu-id="8a3f4-132">Die Azure-Ressourcen-ID für die Bastion, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a3f4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a3f4-133">-WhatIf</span></span>
<span data-ttu-id="8a3f4-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a3f4-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a3f4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a3f4-136">CommonParameters</span></span>
<span data-ttu-id="8a3f4-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a3f4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a3f4-138">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a3f4-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a3f4-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a3f4-139">INPUTS</span></span>

### <span data-ttu-id="8a3f4-140">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="8a3f4-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="8a3f4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8a3f4-141">System.String</span></span>

## <span data-ttu-id="8a3f4-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a3f4-142">OUTPUTS</span></span>

### <span data-ttu-id="8a3f4-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a3f4-143">System.Boolean</span></span>

## <span data-ttu-id="8a3f4-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a3f4-144">NOTES</span></span>

## <span data-ttu-id="8a3f4-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a3f4-145">RELATED LINKS</span></span>
[<span data-ttu-id="8a3f4-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="8a3f4-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="8a3f4-147">Neu – AzBastion</span><span class="sxs-lookup"><span data-stu-id="8a3f4-147">New-AzBastion</span></span>](./New-AzBastion.md)