---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 596B8A6F-D3C2-4170-BCD7-B7A1CDB656D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee767e1ba4c5008837e7cef98aafa4017465829
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006279"
---
# <span data-ttu-id="8bdc8-101">Restart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-101">Restart-AzureVM</span></span>

## <span data-ttu-id="8bdc8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bdc8-102">SYNOPSIS</span></span>
<span data-ttu-id="8bdc8-103">Startet einen virtuellen Azure-Computer neu.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="8bdc8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bdc8-104">SYNTAX</span></span>

### <span data-ttu-id="8bdc8-105">RestartByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bdc8-105">RestartByName (Default)</span></span>
```
Restart-AzureVM [-Name] <String> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bdc8-106">RedeployByName</span><span class="sxs-lookup"><span data-stu-id="8bdc8-106">RedeployByName</span></span>
```
Restart-AzureVM [-Name] <String> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bdc8-107">InitiateMaintenanceByName</span><span class="sxs-lookup"><span data-stu-id="8bdc8-107">InitiateMaintenanceByName</span></span>
```
Restart-AzureVM [-Name] <String> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bdc8-108">RestartInput</span><span class="sxs-lookup"><span data-stu-id="8bdc8-108">RestartInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bdc8-109">RedeployInput</span><span class="sxs-lookup"><span data-stu-id="8bdc8-109">RedeployInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-Redeploy] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="8bdc8-110">InitiateMaintenanceInput</span><span class="sxs-lookup"><span data-stu-id="8bdc8-110">InitiateMaintenanceInput</span></span>
```
Restart-AzureVM -VM <PersistentVM> [-InitiateMaintenance] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8bdc8-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bdc8-111">DESCRIPTION</span></span>
<span data-ttu-id="8bdc8-112">Das Cmdlet " **Restart-AzureVM** " fordert einen Neustart eines virtuellen Azure-Computers an.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-112">The **Restart-AzureVM** cmdlet requests a restart of an Azure virtual machine.</span></span>

## <span data-ttu-id="8bdc8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bdc8-113">EXAMPLES</span></span>

### <span data-ttu-id="8bdc8-114">Beispiel 1: Erneutes Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="8bdc8-114">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureVM -ServiceName "MyService01" -Name "MyVM"
```

<span data-ttu-id="8bdc8-115">Mit diesem Befehl wird der virtuelle VirtualMachine27-Computer neu gestartet, der im Azure-Dienst mit dem Namen Service01 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-115">This command restarts the VirtualMachine27 virtual machine running in the Azure service named Service01.</span></span>

### <span data-ttu-id="8bdc8-116">Beispiel 2: Starten eines virtuellen Computers mit einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="8bdc8-116">Example 2: Restart a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MyService01" -Name "VirtualMachine27" | Restart-AzureVM
```

<span data-ttu-id="8bdc8-117">Dieser Befehl ruft das Virtual Machine-Objekt für den virtuellen Computer mit dem Namen MyVM ab und startet es anschließend neu.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-117">This command retrieves the virtual machine object for the virtual machine named MyVM and then restarts it.</span></span>

## <span data-ttu-id="8bdc8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bdc8-118">PARAMETERS</span></span>

### <span data-ttu-id="8bdc8-119">-Information</span><span class="sxs-lookup"><span data-stu-id="8bdc8-119">-InformationAction</span></span>
<span data-ttu-id="8bdc8-120">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8bdc8-121">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8bdc8-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8bdc8-122">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="8bdc8-122">Continue</span></span>
- <span data-ttu-id="8bdc8-123">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="8bdc8-123">Ignore</span></span>
- <span data-ttu-id="8bdc8-124">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="8bdc8-124">Inquire</span></span>
- <span data-ttu-id="8bdc8-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8bdc8-125">SilentlyContinue</span></span>
- <span data-ttu-id="8bdc8-126">Beenden</span><span class="sxs-lookup"><span data-stu-id="8bdc8-126">Stop</span></span>
- <span data-ttu-id="8bdc8-127">Anhalten</span><span class="sxs-lookup"><span data-stu-id="8bdc8-127">Suspend</span></span>

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

### <span data-ttu-id="8bdc8-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8bdc8-128">-InformationVariable</span></span>
<span data-ttu-id="8bdc8-129">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8bdc8-130">-InitiateMaintenance</span><span class="sxs-lookup"><span data-stu-id="8bdc8-130">-InitiateMaintenance</span></span>
<span data-ttu-id="8bdc8-131">Initiieren der Wartung auf dem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="8bdc8-131">Initiate Maintenance on the Virtual Machine</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: InitiateMaintenanceByName, InitiateMaintenanceInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdc8-132">-Name</span><span class="sxs-lookup"><span data-stu-id="8bdc8-132">-Name</span></span>
<span data-ttu-id="8bdc8-133">Gibt den Namen des virtuellen Computers an, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-133">Specifies the name of the virtual machine to restart.</span></span>

```yaml
Type: String
Parameter Sets: RestartByName, RedeployByName, InitiateMaintenanceByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdc8-134">-Profil</span><span class="sxs-lookup"><span data-stu-id="8bdc8-134">-Profile</span></span>
<span data-ttu-id="8bdc8-135">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8bdc8-136">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8bdc8-137">– Erneute Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="8bdc8-137">-Redeploy</span></span>
<span data-ttu-id="8bdc8-138">Gibt an, dass das Cmdlet den virtuellen Computer erneut bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-138">Indicates that the cmdlet redeploys the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployByName, RedeployInput
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bdc8-139">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8bdc8-139">-ServiceName</span></span>
<span data-ttu-id="8bdc8-140">Gibt den Namen des Azure-Diensts an, der den virtuellen Computer enthält, der neu gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-140">Specifies the name of the Azure service that contains the virtual machine to restart.</span></span>

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

### <span data-ttu-id="8bdc8-141">-VM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-141">-VM</span></span>
<span data-ttu-id="8bdc8-142">Gibt ein Objekt eines virtuellen Computers an, das den Neustart des virtuellen Computers kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-142">Specifies a virtual machine object that identifies the virtual machine to restart.</span></span>

```yaml
Type: PersistentVM
Parameter Sets: RestartInput, RedeployInput, InitiateMaintenanceInput
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8bdc8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bdc8-143">CommonParameters</span></span>
<span data-ttu-id="8bdc8-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bdc8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bdc8-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bdc8-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bdc8-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bdc8-146">INPUTS</span></span>

## <span data-ttu-id="8bdc8-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bdc8-147">OUTPUTS</span></span>

## <span data-ttu-id="8bdc8-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bdc8-148">NOTES</span></span>

## <span data-ttu-id="8bdc8-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bdc8-149">RELATED LINKS</span></span>

[<span data-ttu-id="8bdc8-150">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-150">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="8bdc8-151">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-151">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="8bdc8-152">Anfang-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-152">Start-AzureVM</span></span>](./Start-AzureVM.md)

[<span data-ttu-id="8bdc8-153">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-153">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="8bdc8-154">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="8bdc8-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


