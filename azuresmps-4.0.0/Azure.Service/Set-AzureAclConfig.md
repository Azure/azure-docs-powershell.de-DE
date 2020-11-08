---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A9E43722-DEE2-4A5C-A3F6-8DA6612735AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 34e6e98c2bf506e8102287251e18dceda4dd0c7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006638"
---
# <span data-ttu-id="f127e-101">Set-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f127e-101">Set-AzureAclConfig</span></span>

## <span data-ttu-id="f127e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f127e-102">SYNOPSIS</span></span>
<span data-ttu-id="f127e-103">Ändert ein ACL-Konfigurationsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f127e-103">Modifies an ACL configuration object.</span></span>

## <span data-ttu-id="f127e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f127e-104">SYNTAX</span></span>

### <span data-ttu-id="f127e-105">AddRule</span><span class="sxs-lookup"><span data-stu-id="f127e-105">AddRule</span></span>
```
Set-AzureAclConfig [-AddRule] [-Action] <String> [-RemoteSubnet] <String> [[-Order] <Int32>]
 [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f127e-106">RemoveRule</span><span class="sxs-lookup"><span data-stu-id="f127e-106">RemoveRule</span></span>
```
Set-AzureAclConfig [-RemoveRule] [-RuleId] <Int32> -ACL <NetworkAclObject>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f127e-107">Setrule</span><span class="sxs-lookup"><span data-stu-id="f127e-107">SetRule</span></span>
```
Set-AzureAclConfig [-SetRule] [-RuleId] <Int32> [[-Action] <String>] [[-RemoteSubnet] <String>]
 [[-Order] <Int32>] [[-Description] <String>] -ACL <NetworkAclObject> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f127e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f127e-108">DESCRIPTION</span></span>
<span data-ttu-id="f127e-109">Das Cmdlet " **festlegen-AzureAclConfig** " ändert ein Configuration-Objekt für die Zugriffssteuerungsliste (ACL) aus einer vorhandenen Azure Virtual Machine-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f127e-109">The **Set-AzureAclConfig** cmdlet modifies an access control list (ACL) configuration object from an existing Azure virtual machine configuration.</span></span>

## <span data-ttu-id="f127e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f127e-110">EXAMPLES</span></span>

### <span data-ttu-id="f127e-111">Beispiel 1: Hinzufügen einer Regel zu einer neuen ACL-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f127e-111">Example 1: Add a rule to a new ACL configuration</span></span>
```
PS C:\> $Acl = New-AzureAclConfig
PS C:\> Set-AzureAclConfig -AddRule -ACL $Acl -Action Permit -RemoteSubnet "172.0.0.0/8" -Order 100 -Description "Permit ACL rule"
```

<span data-ttu-id="f127e-112">Der erste Befehl erstellt eine ACL-Konfiguration und speichert Sie dann in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f127e-112">The first command creates an ACL configuration, and then stores it in the $Acl variable.</span></span>

<span data-ttu-id="f127e-113">Mit dem zweiten Befehl wird der in $ACL gespeicherten Konfiguration eine neue Regel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f127e-113">The second command adds a new rule to the configuration stored in $Acl.</span></span>
<span data-ttu-id="f127e-114">Der Befehl gibt eine Aktion, ein Subnetz, eine Reihenfolge und eine Beschreibung für die Regel an.</span><span class="sxs-lookup"><span data-stu-id="f127e-114">The command specifies an action, subnet, order, and description for the rule.</span></span>

### <span data-ttu-id="f127e-115">Beispiel 2: Ändern einer Regel in einer ACL-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f127e-115">Example 2: Modify a rule in an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -SetRule -RuleId 0 -ACL $Acl -Order 102 -Description "Web endpoint rule"
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="f127e-116">Der erste Befehl ruft den virtuellen Computer mit dem Namen VirtualMachine07 im Dienst ContosoService mit dem Cmdlet **Get-AzureVM** ab.</span><span class="sxs-lookup"><span data-stu-id="f127e-116">The first command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="f127e-117">Der Befehl übergibt dieses Objekt mithilfe des Pipelineoperators an das Cmdlet " **Get-AzureAclConfig** ".</span><span class="sxs-lookup"><span data-stu-id="f127e-117">The command passes that object to the **Get-AzureAclConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f127e-118">Dieses Cmdlet ruft die ACL-Konfiguration für den Endpunkt mit dem Namen Web ab.</span><span class="sxs-lookup"><span data-stu-id="f127e-118">That cmdlet gets the ACL configuration for the endpoint named Web.</span></span>
<span data-ttu-id="f127e-119">Der Befehl speichert das ACL-Konfigurationsobjekt in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f127e-119">The command stores that ACL configuration object in the $Acl variable.</span></span>

<span data-ttu-id="f127e-120">Der zweite Befehl ändert die Regel, die die ID 0 hat.</span><span class="sxs-lookup"><span data-stu-id="f127e-120">The second command modifies the rule that has the ID of 0.</span></span>
<span data-ttu-id="f127e-121">Der Befehl ändert die Reihenfolge und die Beschreibung der Regel.</span><span class="sxs-lookup"><span data-stu-id="f127e-121">The command changes the order and the description of the rule.</span></span>

<span data-ttu-id="f127e-122">Der endgültige Befehl legt das ACL-Konfigurationsobjekt für diesen virtuellen Computer mithilfe des Cmdlets " **Set-AzureEndpoint** " fest.</span><span class="sxs-lookup"><span data-stu-id="f127e-122">The final command sets the ACL configuration object for that virtual machine by using the **Set-AzureEndpoint** cmdlet.</span></span>
<span data-ttu-id="f127e-123">Der Befehl aktualisiert auch diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f127e-123">The command also updates that virtual machine.</span></span>

### <span data-ttu-id="f127e-124">Beispiel 3: Entfernen einer Regel aus einer ACL-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="f127e-124">Example 3: Remove a rule from an ACL configuration</span></span>
```
PS C:\> $Acl = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Get-AzureAclConfig -EndpointName "Web"
PS C:\> Set-AzureAclConfig -RemoveRule -ID 0 -ACL $Acl
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Set-AzureEndpoint -ACL $Acl -Name "Web" | Update-AzureVM
```

<span data-ttu-id="f127e-125">Der erste Befehl speichert ein ACL-Konfigurationsobjekt in der $ACL-Variablen.</span><span class="sxs-lookup"><span data-stu-id="f127e-125">The first command stores an ACL configuration object in the $Acl variable.</span></span>
<span data-ttu-id="f127e-126">Dies entspricht dem vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f127e-126">This is the same as the previous example.</span></span>

<span data-ttu-id="f127e-127">Der zweite Befehl entfernt die Regel, die die ID 0 hat, aus der ACL-Konfiguration in $ACL.</span><span class="sxs-lookup"><span data-stu-id="f127e-127">The second command removes the rule that has the ID 0 from the ACL configuration in $Acl.</span></span>

<span data-ttu-id="f127e-128">Der endgültige Befehl legt das ACL-Konfigurationsobjekt für den virtuellen Computer fest und aktualisiert diesen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="f127e-128">The final command sets the ACL configuration object for the virtual machine and updates that virtual machine.</span></span>
<span data-ttu-id="f127e-129">Dies entspricht dem vorherigen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f127e-129">This is the same as the previous example.</span></span>

## <span data-ttu-id="f127e-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="f127e-130">PARAMETERS</span></span>

### <span data-ttu-id="f127e-131">-ACL</span><span class="sxs-lookup"><span data-stu-id="f127e-131">-ACL</span></span>
<span data-ttu-id="f127e-132">Gibt ein ACL-Konfigurationsobjekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f127e-132">Specifies an ACL configuration object that this cmdlet modifies.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-133">– Aktion</span><span class="sxs-lookup"><span data-stu-id="f127e-133">-Action</span></span>
<span data-ttu-id="f127e-134">Gibt die Aktion für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f127e-134">Specifies the action for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="f127e-135">Gültige Werte sind: zulassen und verweigern.</span><span class="sxs-lookup"><span data-stu-id="f127e-135">Valid values are: Permit and Deny.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-136">-AddRule</span><span class="sxs-lookup"><span data-stu-id="f127e-136">-AddRule</span></span>
<span data-ttu-id="f127e-137">Gibt an, dass dieses Cmdlet der ACL-Konfiguration eine Regel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="f127e-137">Indicates that this cmdlet adds a rule to the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AddRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-138">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f127e-138">-Description</span></span>
<span data-ttu-id="f127e-139">Gibt eine Beschreibung für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f127e-139">Specifies a description for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-140">-Information</span><span class="sxs-lookup"><span data-stu-id="f127e-140">-InformationAction</span></span>
<span data-ttu-id="f127e-141">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f127e-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f127e-142">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f127e-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f127e-143">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f127e-143">Continue</span></span>
- <span data-ttu-id="f127e-144">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f127e-144">Ignore</span></span>
- <span data-ttu-id="f127e-145">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f127e-145">Inquire</span></span>
- <span data-ttu-id="f127e-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f127e-146">SilentlyContinue</span></span>
- <span data-ttu-id="f127e-147">Beenden</span><span class="sxs-lookup"><span data-stu-id="f127e-147">Stop</span></span>
- <span data-ttu-id="f127e-148">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f127e-148">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f127e-149">-InformationVariable</span></span>
<span data-ttu-id="f127e-150">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f127e-150">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-151">-Bestellung</span><span class="sxs-lookup"><span data-stu-id="f127e-151">-Order</span></span>
<span data-ttu-id="f127e-152">Gibt die Verarbeitungsreihenfolge für die Regel an, die von diesem Cmdlet hinzugefügt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f127e-152">Specifies the processing order for the rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: AddRule, SetRule
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-153">-RemoteSubnet</span><span class="sxs-lookup"><span data-stu-id="f127e-153">-RemoteSubnet</span></span>
<span data-ttu-id="f127e-154">Gibt das Remote-Subnetz für die Regel an, die dieses Cmdlet hinzufügt oder ändert.</span><span class="sxs-lookup"><span data-stu-id="f127e-154">Specifies the remote subnet for the rule that this cmdlet adds or modifies.</span></span>
<span data-ttu-id="f127e-155">Gibt eine Adresse im CIDR-Format (classlos InterDomain Routing) an.</span><span class="sxs-lookup"><span data-stu-id="f127e-155">Specifies an address in Classless Interdomain Routing (CIDR) format.</span></span>

```yaml
Type: String
Parameter Sets: AddRule
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetRule
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-156">-RemoveRule</span><span class="sxs-lookup"><span data-stu-id="f127e-156">-RemoveRule</span></span>
<span data-ttu-id="f127e-157">Gibt an, dass dieses Cmdlet eine Regel aus der ACL-Konfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="f127e-157">Indicates that this cmdlet removes a rule from the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-158">-Lineal</span><span class="sxs-lookup"><span data-stu-id="f127e-158">-RuleId</span></span>
<span data-ttu-id="f127e-159">Gibt die ID der Regel an, die dieses Cmdlet für die ACL-Konfiguration entfernt oder ändert.</span><span class="sxs-lookup"><span data-stu-id="f127e-159">Specifies the ID of the rule that this cmdlet removes or modifies for the ACL configuration.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveRule, SetRule
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-160">-Setrule</span><span class="sxs-lookup"><span data-stu-id="f127e-160">-SetRule</span></span>
<span data-ttu-id="f127e-161">Gibt an, dass mit diesem Cmdlet eine Regel in der ACL-Konfiguration geändert wird.</span><span class="sxs-lookup"><span data-stu-id="f127e-161">Indicates that this cmdlet modifies a rule in the ACL configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetRule
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f127e-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f127e-162">CommonParameters</span></span>
<span data-ttu-id="f127e-163">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f127e-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f127e-164">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f127e-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f127e-165">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f127e-165">INPUTS</span></span>

## <span data-ttu-id="f127e-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f127e-166">OUTPUTS</span></span>

## <span data-ttu-id="f127e-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="f127e-167">NOTES</span></span>

## <span data-ttu-id="f127e-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f127e-168">RELATED LINKS</span></span>

[<span data-ttu-id="f127e-169">Get-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f127e-169">Get-AzureAclConfig</span></span>](./Get-AzureAclConfig.md)

[<span data-ttu-id="f127e-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f127e-170">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f127e-171">Neu – AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f127e-171">New-AzureAclConfig</span></span>](./New-AzureAclConfig.md)

[<span data-ttu-id="f127e-172">Remove-AzureAclConfig</span><span class="sxs-lookup"><span data-stu-id="f127e-172">Remove-AzureAclConfig</span></span>](./Remove-AzureAclConfig.md)

[<span data-ttu-id="f127e-173">Satz-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="f127e-173">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="f127e-174">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f127e-174">Update-AzureVM</span></span>](./Update-AzureVM.md)


