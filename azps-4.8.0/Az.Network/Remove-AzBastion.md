---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174308"
---
# <span data-ttu-id="887fd-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="887fd-101">Remove-AzBastion</span></span>

## <span data-ttu-id="887fd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="887fd-102">SYNOPSIS</span></span>
<span data-ttu-id="887fd-103">Entfernt eine Bastions Ressource.</span><span class="sxs-lookup"><span data-stu-id="887fd-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="887fd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="887fd-104">SYNTAX</span></span>

### <span data-ttu-id="887fd-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="887fd-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887fd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="887fd-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="887fd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="887fd-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="887fd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="887fd-108">DESCRIPTION</span></span>
<span data-ttu-id="887fd-109">Entfernt eine Bastions Ressource. Beispiel1 löscht die Bastion mithilfe der ResourceGroupName-und resourceName-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="887fd-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="887fd-110">Example2 löscht die Bastion mithilfe Ihres Objekts mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="887fd-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="887fd-111">Example3 löscht die Bastion mithilfe Ihres Objekts.</span><span class="sxs-lookup"><span data-stu-id="887fd-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="887fd-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="887fd-112">EXAMPLES</span></span>

### <span data-ttu-id="887fd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="887fd-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="887fd-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="887fd-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="887fd-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="887fd-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="887fd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="887fd-116">PARAMETERS</span></span>

### <span data-ttu-id="887fd-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="887fd-117">-Confirm</span></span>
<span data-ttu-id="887fd-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="887fd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="887fd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="887fd-119">-DefaultProfile</span></span>
<span data-ttu-id="887fd-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="887fd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="887fd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="887fd-121">-Force</span></span>
<span data-ttu-id="887fd-122">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="887fd-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="887fd-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="887fd-123">-InputObject</span></span>
<span data-ttu-id="887fd-124">Das zu löschende Bastion-Objekt.</span><span class="sxs-lookup"><span data-stu-id="887fd-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="887fd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="887fd-125">-Name</span></span>
<span data-ttu-id="887fd-126">Der Name der zu löschenden Bastion-Ressource.</span><span class="sxs-lookup"><span data-stu-id="887fd-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="887fd-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="887fd-127">-PassThru</span></span>
<span data-ttu-id="887fd-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="887fd-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="887fd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="887fd-129">-ResourceGroupName</span></span>
<span data-ttu-id="887fd-130">Der Ressourcengruppenname, in dem Bastion vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="887fd-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="887fd-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="887fd-131">-ResourceId</span></span>
<span data-ttu-id="887fd-132">Die Azure-Ressourcen-ID für die Bastion, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="887fd-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="887fd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="887fd-133">-WhatIf</span></span>
<span data-ttu-id="887fd-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="887fd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="887fd-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="887fd-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="887fd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="887fd-136">CommonParameters</span></span>
<span data-ttu-id="887fd-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="887fd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="887fd-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="887fd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="887fd-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="887fd-139">INPUTS</span></span>

### <span data-ttu-id="887fd-140">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="887fd-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="887fd-141">System. String</span><span class="sxs-lookup"><span data-stu-id="887fd-141">System.String</span></span>

## <span data-ttu-id="887fd-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="887fd-142">OUTPUTS</span></span>

### <span data-ttu-id="887fd-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="887fd-143">System.Boolean</span></span>

## <span data-ttu-id="887fd-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="887fd-144">NOTES</span></span>

## <span data-ttu-id="887fd-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="887fd-145">RELATED LINKS</span></span>
[<span data-ttu-id="887fd-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="887fd-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="887fd-147">Neu – AzBastion</span><span class="sxs-lookup"><span data-stu-id="887fd-147">New-AzBastion</span></span>](./New-AzBastion.md)