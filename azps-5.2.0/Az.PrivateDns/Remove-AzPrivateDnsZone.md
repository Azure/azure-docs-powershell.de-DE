---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsZone.md
ms.openlocfilehash: d381af8de23b5eb781882f10670e6ba69afbc571
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98303595"
---
# <span data-ttu-id="f210c-101">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f210c-101">Remove-AzPrivateDnsZone</span></span>

## <span data-ttu-id="f210c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f210c-102">SYNOPSIS</span></span>
<span data-ttu-id="f210c-103">Entfernt eine private DNS-Zone aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f210c-103">Removes a private DNS zone from a resource group.</span></span>

## <span data-ttu-id="f210c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f210c-104">SYNTAX</span></span>

### <span data-ttu-id="f210c-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="f210c-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsZone -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f210c-106">Objekt</span><span class="sxs-lookup"><span data-stu-id="f210c-106">Object</span></span>
```
Remove-AzPrivateDnsZone -PrivateZone <PSPrivateDnsZone> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f210c-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f210c-107">ResourceId</span></span>
```
Remove-AzPrivateDnsZone -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f210c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f210c-108">DESCRIPTION</span></span>
<span data-ttu-id="f210c-109">Das **Cmdlet "Remove-AzPrivateDnsZone"** löscht eine Private Domain Name System (DNS)-Zone dauerhaft aus einer angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f210c-109">The **Remove-AzPrivateDnsZone** cmdlet permanently deletes a private Domain Name System (DNS) zone from a specified resource group.</span></span>
<span data-ttu-id="f210c-110">Alle in der Zone enthaltenen Datensatzsätze werden ebenfalls gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f210c-110">All record sets contained in the zone are also deleted.</span></span>
<span data-ttu-id="f210c-111">Sie können ein **PrivateDnsZone-Objekt** mit dem *Parameter "PrivateZone"* oder mit dem Pipelineoperator übergeben, oder Sie können die Parameter *"Name"* und *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f210c-111">You can pass a **PrivateDnsZone** object using the *PrivateZone* parameter or by using the pipeline operator, or alternatively you can specify the *Name* and *ResourceGroupName* parameters.</span></span>
<span data-ttu-id="f210c-112">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="f210c-112">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="f210c-113">Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (das über die Pipeline oder den *Parameter "Zone"* übergeben wird), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, da das lokale **"PrivateDnsZone"-Objekt** abgerufen wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="f210c-113">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f210c-114">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="f210c-114">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f210c-115">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="f210c-115">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

## <span data-ttu-id="f210c-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f210c-116">EXAMPLES</span></span>

### <span data-ttu-id="f210c-117">Beispiel 1: Entfernen einer privaten Zone</span><span class="sxs-lookup"><span data-stu-id="f210c-117">Example 1: Remove a private zone</span></span>
```
PS C:\>Remove-AzPrivateDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f210c-118">Mit diesem Befehl wird die Zone namens "myzone.com" aus der Ressourcengruppe "MyResourceGroup" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f210c-118">This command removes the zone named myzone.com from the resource group named MyResourceGroup.</span></span>

## <span data-ttu-id="f210c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f210c-119">PARAMETERS</span></span>

### <span data-ttu-id="f210c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f210c-120">-DefaultProfile</span></span>
<span data-ttu-id="f210c-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f210c-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f210c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f210c-122">-Name</span></span>
<span data-ttu-id="f210c-123">Gibt den Namen der privaten DNS-Zone an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="f210c-123">Specifies the name of the private DNS zone that this cmdlet removes.</span></span>
<span data-ttu-id="f210c-124">Sie müssen auch den Parameter *"ResourceGroupName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f210c-124">You must also specify the *ResourceGroupName* parameter.</span></span>
<span data-ttu-id="f210c-125">Alternativ können Sie die DNS-Zone mit dem Parameter *"Zone"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f210c-125">Alternatively, you can specify the DNS zone using the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-126">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="f210c-126">-Overwrite</span></span>
<span data-ttu-id="f210c-127">Wenn Sie die Zone mit einem **PrivateDnsZone-Objekt** angeben (das über die Pipeline oder den *Parameter "Zone"* übergeben wird), wird die Zone nicht gelöscht, wenn sie in Azure DNS geändert wurde, da das lokale **"PrivateDnsZone"-Objekt** abgerufen wurde (nur Vorgänge direkt für die DNS-Zonenressourcen zählen als Änderungen, Vorgänge für Datensatzsätze innerhalb der Zone nicht).</span><span class="sxs-lookup"><span data-stu-id="f210c-127">When specifying the zone using a **PrivateDnsZone** object (passed via the pipeline or *Zone* parameter), the zone is not deleted if it has been changed in Azure DNS since the local **PrivateDnsZone** object was retrieved (only operations directly on the DNS zone resource count as changes, operations on record sets within the zone do not).</span></span>
<span data-ttu-id="f210c-128">Dies bietet Schutz für Änderungen gleichzeitiger Zonen.</span><span class="sxs-lookup"><span data-stu-id="f210c-128">This provides protection for concurrent zone changes.</span></span>
<span data-ttu-id="f210c-129">Dies kann mithilfe des Parameters *"Overwrite"* unterdrückt werden, der die Zone unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="f210c-129">This can be suppressed using the *Overwrite* parameter, which deletes the zone regardless of concurrent changes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Object
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f210c-130">-PassThru</span></span>
<span data-ttu-id="f210c-131">Wird verwendet, um das Ergebnis (boolesch) des Vorgangs weiter unten in der Pipeline zu löschen.</span><span class="sxs-lookup"><span data-stu-id="f210c-131">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="f210c-132">-PrivateZone</span><span class="sxs-lookup"><span data-stu-id="f210c-132">-PrivateZone</span></span>
<span data-ttu-id="f210c-133">Das private Zonenobjekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="f210c-133">The private zone object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f210c-134">-ResourceGroupName</span></span>
<span data-ttu-id="f210c-135">Gibt den Namen der Ressourcengruppe an, die die zu entfernende Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="f210c-135">Specifies the name of the resource group that contains the zone to remove.</span></span>
<span data-ttu-id="f210c-136">Sie müssen auch den *Parameter "ZoneName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="f210c-136">You must also specify the *ZoneName* parameter.</span></span>
<span data-ttu-id="f210c-137">Alternativ können Sie die DNS-Zone mit einem **PrivateDnsZone-Objekt** angeben, das entweder über die Pipeline oder den Parameter *"Zone" übergeben* wird.</span><span class="sxs-lookup"><span data-stu-id="f210c-137">Alternatively, you can specify the DNS zone using a **PrivateDnsZone** object, passed via either the pipeline or the *Zone* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f210c-138">-ResourceId</span></span>
<span data-ttu-id="f210c-139">Private DNS Zone ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f210c-139">Private DNS Zone ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f210c-140">-Confirm</span></span>
<span data-ttu-id="f210c-141">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f210c-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-142">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f210c-142">-WhatIf</span></span>
<span data-ttu-id="f210c-143">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f210c-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f210c-144">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f210c-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f210c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f210c-145">CommonParameters</span></span>
<span data-ttu-id="f210c-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f210c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f210c-147">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f210c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f210c-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f210c-148">INPUTS</span></span>

### <span data-ttu-id="f210c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f210c-149">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="f210c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f210c-150">System.String</span></span>

## <span data-ttu-id="f210c-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f210c-151">OUTPUTS</span></span>

### <span data-ttu-id="f210c-152">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f210c-152">System.Boolean</span></span>

## <span data-ttu-id="f210c-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f210c-153">NOTES</span></span>

## <span data-ttu-id="f210c-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f210c-154">RELATED LINKS</span></span>

[<span data-ttu-id="f210c-155">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f210c-155">Get-AzPrivateDnsZone</span></span>](./Get-AzPrivateDnsZone.md)

[<span data-ttu-id="f210c-156">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f210c-156">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="f210c-157">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="f210c-157">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
