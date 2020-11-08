---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 455DB2C0-08A0-4D62-B8EE-7C3DB9AD8A8C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85040f07914aef02355f69baab093c75ce7e4afd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005722"
---
# <span data-ttu-id="a00bc-101">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-101">Remove-AzureVM</span></span>

## <span data-ttu-id="a00bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a00bc-102">SYNOPSIS</span></span>
<span data-ttu-id="a00bc-103">Entfernt einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="a00bc-103">Removes an Azure virtual machine.</span></span>

## <span data-ttu-id="a00bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a00bc-104">SYNTAX</span></span>

```
Remove-AzureVM [-Name] <String> [-DeleteVHD] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a00bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a00bc-105">DESCRIPTION</span></span>
<span data-ttu-id="a00bc-106">Das Cmdlet **Remove-AzureVM** löscht einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="a00bc-106">The **Remove-AzureVM** cmdlet deletes an Azure virtual machine.</span></span>
<span data-ttu-id="a00bc-107">Durch diesen Vorgang werden die zugrunde liegenden VHD-Dateien der auf diesem virtuellen Computer bereitgestellten Datenträger nicht gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a00bc-107">This process does not delete the underlying .vhd files of the disks mounted on that virtual machine.</span></span>

## <span data-ttu-id="a00bc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a00bc-108">EXAMPLES</span></span>

### <span data-ttu-id="a00bc-109">Beispiel 1: Entfernen eines virtuellen Computers aus einem Dienst</span><span class="sxs-lookup"><span data-stu-id="a00bc-109">Example 1: Remove a virtual machine from a service</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine03"
```

<span data-ttu-id="a00bc-110">Dieser Befehl entfernt den virtuellen Computer mit dem Namen VirtualMachine03, der im ContosoService03-Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a00bc-110">This command removes the virtual machine named VirtualMachine03 that runs in the ContosoService03 service.</span></span>

### <span data-ttu-id="a00bc-111">Beispiel 2: Entfernen eines virtuellen Computers und Löschen der VHD-Dateien</span><span class="sxs-lookup"><span data-stu-id="a00bc-111">Example 2: Remove a virtual machine and delete the .vhd files</span></span>
```
PS C:\> Remove-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04" -DeleteVHD
```

<span data-ttu-id="a00bc-112">Dieser Befehl entfernt den virtuellen VirtualMachine04-Computer, der im ContosoService03-Dienst ausgeführt wird, und gibt an, dass die VHD-Dateien mithilfe des *DeleteVHD* -Parameters entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a00bc-112">This command removes the VirtualMachine04 virtual machine that runs in the ContosoService03 service, and specifies to remove the .vhd files using the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="a00bc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a00bc-113">PARAMETERS</span></span>

### <span data-ttu-id="a00bc-114">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="a00bc-114">-DeleteVHD</span></span>
<span data-ttu-id="a00bc-115">Gibt an, ob das Cmdlet den virtuellen Computer und die zugrunde liegenden Datenträger-BLOBs entfernt.</span><span class="sxs-lookup"><span data-stu-id="a00bc-115">Specifies whether this cmdlet removes the virtual machine and the underlying disk blobs.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-116">-Information</span><span class="sxs-lookup"><span data-stu-id="a00bc-116">-InformationAction</span></span>
<span data-ttu-id="a00bc-117">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="a00bc-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a00bc-118">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a00bc-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a00bc-119">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="a00bc-119">Continue</span></span>
- <span data-ttu-id="a00bc-120">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="a00bc-120">Ignore</span></span>
- <span data-ttu-id="a00bc-121">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="a00bc-121">Inquire</span></span>
- <span data-ttu-id="a00bc-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a00bc-122">SilentlyContinue</span></span>
- <span data-ttu-id="a00bc-123">Beenden</span><span class="sxs-lookup"><span data-stu-id="a00bc-123">Stop</span></span>
- <span data-ttu-id="a00bc-124">Anhalten</span><span class="sxs-lookup"><span data-stu-id="a00bc-124">Suspend</span></span>

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

### <span data-ttu-id="a00bc-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a00bc-125">-InformationVariable</span></span>
<span data-ttu-id="a00bc-126">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="a00bc-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a00bc-127">-Name</span><span class="sxs-lookup"><span data-stu-id="a00bc-127">-Name</span></span>
<span data-ttu-id="a00bc-128">Gibt den Namen der zu entfernende virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a00bc-128">Specifies the name of the virtual machine being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="a00bc-129">-Profile</span></span>
<span data-ttu-id="a00bc-130">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a00bc-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a00bc-131">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a00bc-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a00bc-132">-ServiceName</span></span>
<span data-ttu-id="a00bc-133">Gibt den Namen des Azure-Diensts an, aus dem der virtuelle Computer entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="a00bc-133">Specifies the name of the Azure service from which the virtual machine is being removed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a00bc-134">-Confirm</span></span>
<span data-ttu-id="a00bc-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a00bc-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a00bc-136">-WhatIf</span></span>
<span data-ttu-id="a00bc-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a00bc-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a00bc-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a00bc-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a00bc-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a00bc-139">CommonParameters</span></span>
<span data-ttu-id="a00bc-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a00bc-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a00bc-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a00bc-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a00bc-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a00bc-142">INPUTS</span></span>

## <span data-ttu-id="a00bc-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a00bc-143">OUTPUTS</span></span>

## <span data-ttu-id="a00bc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a00bc-144">NOTES</span></span>

## <span data-ttu-id="a00bc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a00bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="a00bc-146">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-146">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="a00bc-147">Neu – AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="a00bc-147">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="a00bc-148">Neustart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-148">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="a00bc-149">Anfang-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-149">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="a00bc-150">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-150">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="a00bc-151">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="a00bc-151">Update-AzureVM</span></span>](./Update-AzureVM.md)


