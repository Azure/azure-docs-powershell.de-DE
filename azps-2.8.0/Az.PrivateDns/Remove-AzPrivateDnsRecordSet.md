---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/remove-azprivatednsrecordset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Remove-AzPrivateDnsRecordSet.md
ms.openlocfilehash: 0b54ebe9650ba8dcd382afd308b21e7c48d1062d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824488"
---
# <span data-ttu-id="25e72-101">Remove-AzPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="25e72-101">Remove-AzPrivateDnsRecordSet</span></span>

## <span data-ttu-id="25e72-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25e72-102">SYNOPSIS</span></span>
<span data-ttu-id="25e72-103">Löscht einen Daten Satz Satz aus einer privaten DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="25e72-103">Deletes a record set from a Private DNS zone.</span></span>

## <span data-ttu-id="25e72-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="25e72-104">SYNTAX</span></span>

### <span data-ttu-id="25e72-105">Felder (Standard)</span><span class="sxs-lookup"><span data-stu-id="25e72-105">Fields (Default)</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceGroupName <String> -ZoneName <String> -Name <String>
 -RecordType <RecordType> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="25e72-106">Gemischt</span><span class="sxs-lookup"><span data-stu-id="25e72-106">Mixed</span></span>
```
Remove-AzPrivateDnsRecordSet -Zone <PSPrivateDnsZone> -Name <String> -RecordType <RecordType> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e72-107">Objekt</span><span class="sxs-lookup"><span data-stu-id="25e72-107">Object</span></span>
```
Remove-AzPrivateDnsRecordSet -RecordSet <PSPrivateDnsRecordSet> [-Overwrite] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e72-108">ResourceId</span><span class="sxs-lookup"><span data-stu-id="25e72-108">ResourceId</span></span>
```
Remove-AzPrivateDnsRecordSet -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e72-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25e72-109">DESCRIPTION</span></span>
<span data-ttu-id="25e72-110">Das Remove-AzPrivateDnsRecordSet-Cmdlet löscht den angegebenen Daten Satz Satz aus der angegebenen Zone.</span><span class="sxs-lookup"><span data-stu-id="25e72-110">The Remove-AzPrivateDnsRecordSet cmdlet deletes the specified record set from the specified zone.</span></span> <span data-ttu-id="25e72-111">Sie können keine SOA-Einträge löschen, die automatisch in der privaten Zone Apex erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="25e72-111">You cannot delete SOA records that are automatically created at the private zone apex.</span></span> <span data-ttu-id="25e72-112">Sie können ein Recordset-Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter oder als eine Hilfsquelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="25e72-112">You can pass a RecordSet object to this cmdlet by using the pipeline operator or as a parameter or as a ResourceId.</span></span> <span data-ttu-id="25e72-113">Um einen Daten Satz Satz nach Name und Typ ohne Verwendung eines Recordset-Objekts zu identifizieren, müssen Sie die Zone als PSPrivateDnsZone-Objekt an dieses Cmdlet übergeben, indem Sie den Pipelineoperator oder als Parameter verwenden, oder Sie können auch die Parameter zonename und ResourceGroupName angeben.</span><span class="sxs-lookup"><span data-stu-id="25e72-113">To identify a record set by name and type without using a RecordSet object, you must pass the zone as a PSPrivateDnsZone object to this cmdlet by using the pipeline operator or as a parameter, or alternatively you can specify the ZoneName and ResourceGroupName parameters.</span></span> <span data-ttu-id="25e72-114">Sie können den Parameter Confirm und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="25e72-114">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span> <span data-ttu-id="25e72-115">Wenn Sie den Daten Satz Satz mit einem Recordset-Objekt angeben, wird der Daten Satz Satz nicht gelöscht, wenn er in Azure private DNS geändert wurde, nachdem das lokale Recordset-Objekt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="25e72-115">When specifying the record set using a RecordSet object, the record set is not deleted if it has been changed in Azure Private DNS since the local RecordSet object was retrieved.</span></span> <span data-ttu-id="25e72-116">Dadurch wird der Schutz für gleichzeitige Änderungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="25e72-116">This provides protection for concurrent changes.</span></span> <span data-ttu-id="25e72-117">Sie können dies unterdrücken, indem Sie den Parameter overwrite verwenden, der den Daten Satz Satz unabhängig von gleichzeitigen Änderungen löscht.</span><span class="sxs-lookup"><span data-stu-id="25e72-117">You can suppress this by using the Overwrite parameter, which deletes the record set regardless of concurrent changes.</span></span>

## <span data-ttu-id="25e72-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25e72-118">EXAMPLES</span></span>

### <span data-ttu-id="25e72-119">Beispiel 1: Entfernen eines Daten Satz Satzes</span><span class="sxs-lookup"><span data-stu-id="25e72-119">Example 1: Remove a record set</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ResourceGroupName "MyResourceGroup" -ZoneName "myzone.com"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet
```

<span data-ttu-id="25e72-120">Der erste Befehl ruft den angegebenen Daten Satz Satz ab und speichert ihn dann in der $Recordset Variablen. Mit dem zweiten Befehl wird der Satz in $Recordset entfernt.</span><span class="sxs-lookup"><span data-stu-id="25e72-120">The first command gets the specified record set, and then stores it in the $RecordSet variable.The second command removes the record set in $RecordSet.</span></span>

### <span data-ttu-id="25e72-121">Beispiel 2: Entfernen eines Daten Satz Satzes und unterdrücken der gesamten Bestätigung</span><span class="sxs-lookup"><span data-stu-id="25e72-121">Example 2: Remove a record set and suppress all confirmation</span></span>
```powershell
PS C:\> $RecordSet = Get-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup"
PS C:\> Remove-AzPrivateDnsRecordSet -RecordSet $RecordSet -Confirm:$False -Overwrite

# Alternatively, the record set can be removed as follows.  In this case,
# because the record set is specified by name rather than by object, the
# Overwrite parameter is not applicable.

PS C:\> Remove-AzPrivateDnsRecordSet -Name "www" -ZoneName "myzone.com" -ResourceGroupName "MyResourceGroup" -Confirm:$False
```

<span data-ttu-id="25e72-122">Der erste Befehl ruft den angegebenen Daten Satz Satz ab.</span><span class="sxs-lookup"><span data-stu-id="25e72-122">The first command gets the specified record set.</span></span> <span data-ttu-id="25e72-123">Der zweite Befehl löscht die Datensatzgruppe, auch wenn Sie sich in der Zwischenzeit geändert hat.</span><span class="sxs-lookup"><span data-stu-id="25e72-123">The second command deletes the record set, even if it has changed in the meantime.</span></span> <span data-ttu-id="25e72-124">Bestätigungsaufforderungen werden unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="25e72-124">Confirmation prompts are suppressed.</span></span>

## <span data-ttu-id="25e72-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="25e72-125">PARAMETERS</span></span>

### <span data-ttu-id="25e72-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e72-126">-DefaultProfile</span></span>
<span data-ttu-id="25e72-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25e72-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e72-128">-Name</span><span class="sxs-lookup"><span data-stu-id="25e72-128">-Name</span></span>
<span data-ttu-id="25e72-129">Der Name der Datensätze in der Datensatzgruppe (relativ zum Namen der Zone und ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="25e72-129">The name of the records in the record set (relative to the name of the zone and without a terminating dot).</span></span>

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

### <span data-ttu-id="25e72-130">-Overwrite</span><span class="sxs-lookup"><span data-stu-id="25e72-130">-Overwrite</span></span>
<span data-ttu-id="25e72-131">Verwenden Sie das ETag-Feld des Recordset-Parameters nicht für Prüfungen mit vollständigen Parallelität.</span><span class="sxs-lookup"><span data-stu-id="25e72-131">Do not use the ETag field of the RecordSet parameter for optimistic concurrency checks.</span></span>

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

### <span data-ttu-id="25e72-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e72-132">-PassThru</span></span>
<span data-ttu-id="25e72-133">Wird verwendet, um das Ergebnis (boolescher Wert) des Vorgangs Delete private Zone weiter unten in der Pipeline zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="25e72-133">Used for passing the result (boolean) of the operation delete private zone further down the pipeline.</span></span>

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

### <span data-ttu-id="25e72-134">-Recordset</span><span class="sxs-lookup"><span data-stu-id="25e72-134">-RecordSet</span></span>
<span data-ttu-id="25e72-135">Die Datensatzgruppe, in der der Datensatz hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25e72-135">The record set in which to add the record.</span></span>

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

### <span data-ttu-id="25e72-136">-RecordType</span><span class="sxs-lookup"><span data-stu-id="25e72-136">-RecordType</span></span>
<span data-ttu-id="25e72-137">Der Typ der privaten DNS-Einträge in der Datensatzgruppe.</span><span class="sxs-lookup"><span data-stu-id="25e72-137">The type of Private DNS records in the record set.</span></span>

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

### <span data-ttu-id="25e72-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e72-138">-ResourceGroupName</span></span>
<span data-ttu-id="25e72-139">Die Ressourcengruppe, zu der die Zone gehört.</span><span class="sxs-lookup"><span data-stu-id="25e72-139">The resource group to which the zone belongs.</span></span>

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

### <span data-ttu-id="25e72-140">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="25e72-140">-ResourceId</span></span>
<span data-ttu-id="25e72-141">Private DNS-Recordset-Quell Code.</span><span class="sxs-lookup"><span data-stu-id="25e72-141">Private DNS RecordSet ResourceID.</span></span>

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

### <span data-ttu-id="25e72-142">-Zone</span><span class="sxs-lookup"><span data-stu-id="25e72-142">-Zone</span></span>
<span data-ttu-id="25e72-143">Das PrivateDnsZone-Objekt, das die Zone darstellt, in der der Daten Satz Satz erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="25e72-143">The PrivateDnsZone object representing the zone in which to create the record set.</span></span>

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

### <span data-ttu-id="25e72-144">-ZoneName</span><span class="sxs-lookup"><span data-stu-id="25e72-144">-ZoneName</span></span>
<span data-ttu-id="25e72-145">Die Zone, in der der Daten Satz Satz vorhanden ist (ohne Endpunkt).</span><span class="sxs-lookup"><span data-stu-id="25e72-145">The zone in which the record set exists (without a terminating dot).</span></span>

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

### <span data-ttu-id="25e72-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="25e72-146">-Confirm</span></span>
<span data-ttu-id="25e72-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e72-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e72-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e72-148">-WhatIf</span></span>
<span data-ttu-id="25e72-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25e72-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e72-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25e72-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e72-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e72-151">CommonParameters</span></span>
<span data-ttu-id="25e72-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e72-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e72-153">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e72-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e72-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25e72-154">INPUTS</span></span>

### <span data-ttu-id="25e72-155">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="25e72-155">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

### <span data-ttu-id="25e72-156">Microsoft. Azure. Commands. PrivateDns. Models. PSPrivateDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="25e72-156">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsRecordSet</span></span>

### <span data-ttu-id="25e72-157">System. String</span><span class="sxs-lookup"><span data-stu-id="25e72-157">System.String</span></span>

## <span data-ttu-id="25e72-158">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25e72-158">OUTPUTS</span></span>

### <span data-ttu-id="25e72-159">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25e72-159">System.Boolean</span></span>

## <span data-ttu-id="25e72-160">Notizen</span><span class="sxs-lookup"><span data-stu-id="25e72-160">NOTES</span></span>

## <span data-ttu-id="25e72-161">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25e72-161">RELATED LINKS</span></span>
