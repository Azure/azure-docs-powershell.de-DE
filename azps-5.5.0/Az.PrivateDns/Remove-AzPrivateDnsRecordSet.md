---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 865ab4ab3cca9d921fc8c40e9c6ae5cd03eaf00a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100153865"
---
# <span data-ttu-id="1fe0d-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1fe0d-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="1fe0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe0d-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe0d-103">Löscht einen Datensatzsatz aus einer privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="1fe0d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fe0d-104">SYNTAX</span></span>

### <span data-ttu-id="1fe0d-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fe0d-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fe0d-106">Gemischt</span><span class="sxs-lookup"><span data-stu-id="1fe0d-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe0d-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="1fe0d-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe0d-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe0d-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe0d-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fe0d-109">DESCRIPTION</span></span>
<span data-ttu-id="1fe0d-110">Das Remove-AzPrivateDnsRecordSet cmdlet löscht den angegebenen Datensatzsatz aus der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="1fe0d-111">Sie können keine SOA-Einträge löschen, die automatisch an der Spitze der privaten Zone erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="1fe0d-112">Sie können ein "RecordSet"-Objekt mithilfe des Pipelineoperators, als Parameter oder als ResourceId an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="1fe0d-113">Zum Identifizieren eines Datensatzes nach Name und Typ ohne Verwendung eines "RecordSet"-Objekts müssen Sie die Zone als "PSPrivateDnsZone"-Objekt mit dem Pipelineoperator oder als Parameter an dieses Cmdlet übergeben. Alternativ können Sie auch die Parameter "ZoneName" und "ResourceGroupName" angeben.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="1fe0d-114">Sie können den Parameter "Bestätigen" und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="1fe0d-115">Wenn Sie den Datensatzsatz mithilfe eines "RecordSet"-Objekts angeben, wird der Datensatzsatz nicht gelöscht, wenn er seit dem Abrufen des lokalen "RecordSet"-Objekts im privaten Azure-DNS geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="1fe0d-116">Dies bietet Schutz für gleichzeitige Änderungen.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="1fe0d-117">Sie können dies unterdrücken, indem Sie den Parameter "Overwrite" verwenden, der den Datensatzsatz unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="1fe0d-118">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fe0d-118">EXAMPLES</span></span>

### <span data-ttu-id="1fe0d-119">Beispiel 1: Entfernen eines Datensatzes</span><span class="sxs-lookup"><span data-stu-id="1fe0d-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="1fe0d-120">Der erste Befehl ruft den angegebenen Datensatzsatz ab und speichert ihn dann in der $RecordSet Variable. Der zweite Befehl entfernt den Datensatzsatz in $RecordSet.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="1fe0d-121">Beispiel 2: Entfernen eines Datensatzes und Unterdrücken aller Bestätigungen</span><span class="sxs-lookup"><span data-stu-id="1fe0d-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="1fe0d-122">Der erste Befehl ruft den angegebenen Datensatzsatz ab.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-122">The first command gets the specified record set.</span></span> <span data-ttu-id="1fe0d-123">Mit dem zweiten Befehl wird der Datensatzsatz gelöscht, auch wenn er sich in der Zwischenzeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="1fe0d-124">Bestätigungsaufforderungen werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="1fe0d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe0d-125">PARAMETERS</span></span>

### <span data-ttu-id="1fe0d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe0d-126">-DefaultProfile</span></span>
<span data-ttu-id="1fe0d-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe0d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="1fe0d-128">-Name</span></span>
<span data-ttu-id="1fe0d-129">Der Name der Datensätze im Datensatzsatz (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="1fe0d-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

```yaml
Type: System.String
Parameter Sets: Fields, Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe0d-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="1fe0d-130">-Overwrite</span></span>
<span data-ttu-id="1fe0d-131">Verwenden Sie das Feld "ETag" des Parameters "RecordSet" nicht für optimistische Parallelitätsprüfungen.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="1fe0d-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe0d-132">-PassThru</span></span>
<span data-ttu-id="1fe0d-133">Wird verwendet, um das Ergebnis (boolesch) des Vorgangs weiter unten in der Pipeline zu löschen.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="1fe0d-134">-RecordSet</span><span class="sxs-lookup"><span data-stu-id="1fe0d-134">-RecordSet</span></span>
<span data-ttu-id="1fe0d-135">Der Datensatzsatz, in dem der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-135">The record set in which to add the record.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe0d-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="1fe0d-136">-RecordType</span></span>
<span data-ttu-id="1fe0d-137">Der Typ der privaten DNS-Einträge im Datensatzsatz.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-137">The type of Private DNS records in the record set.</span></span>

```yaml
Type: Microsoft.Azure.Management.PrivateDns.Models.RecordType
Parameter Sets: Fields, Mixed
Aliases:
Accepted values: A, AAAA, CNAME, MX, PTR, SOA, SRV, TXT

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fe0d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe0d-138">-ResourceGroupName</span></span>
<span data-ttu-id="1fe0d-139">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="1fe0d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe0d-140">-ResourceId</span></span>
<span data-ttu-id="1fe0d-141">Private DNS RecordSet ResourceID.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="1fe0d-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="1fe0d-142">-Zone</span></span>
<span data-ttu-id="1fe0d-143">Das PrivateDnsZone-Objekt, das die Zone darstellt, in der der Datensatzsatz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone
Parameter Sets: Mixed
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fe0d-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="1fe0d-144">-ZoneName</span></span>
<span data-ttu-id="1fe0d-145">Die Zone, in der der Datensatzsatz vorhanden ist (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="1fe0d-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="1fe0d-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fe0d-146">-Confirm</span></span>
<span data-ttu-id="1fe0d-147">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe0d-148">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1fe0d-148">-WhatIf</span></span>
<span data-ttu-id="1fe0d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe0d-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe0d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe0d-151">CommonParameters</span></span>
<span data-ttu-id="1fe0d-152">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe0d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe0d-153">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fe0d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe0d-154">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fe0d-154">INPUTS</span></span>

### <span data-ttu-id="1fe0d-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="1fe0d-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="1fe0d-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="1fe0d-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="1fe0d-157">System.String</span><span class="sxs-lookup"><span data-stu-id="1fe0d-157">System.String</span></span>

## <span data-ttu-id="1fe0d-158">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fe0d-158">OUTPUTS</span></span>

### <span data-ttu-id="1fe0d-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fe0d-159">System.Boolean</span></span>

## <span data-ttu-id="1fe0d-160">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1fe0d-160">NOTES</span></span>

## <span data-ttu-id="1fe0d-161">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1fe0d-161">RELATED LINKS</span></span>
