---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005947"
---
# <span data-ttu-id="85651-101">Stop-AzureVM</span><span class="sxs-lookup"><span data-stu-id="85651-101">Stop-AzureVM</span></span>

## <span data-ttu-id="85651-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85651-102">SYNOPSIS</span></span>
<span data-ttu-id="85651-103">Beendet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="85651-103">Shuts down an Azure virtual machine.</span></span>

## <span data-ttu-id="85651-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85651-104">SYNTAX</span></span>

### <span data-ttu-id="85651-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85651-105">ByName (Default)</span></span>
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="85651-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="85651-106">Input</span></span>
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="85651-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85651-107">DESCRIPTION</span></span>
<span data-ttu-id="85651-108">Das Cmdlet " **Stop-AzureVM** " beendet einen virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="85651-108">The **Stop-AzureVM** cmdlet shuts down a virtual machine.</span></span>

## <span data-ttu-id="85651-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85651-109">EXAMPLES</span></span>

### <span data-ttu-id="85651-110">Beispiel 1: Herunterfahren eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="85651-110">Example 1: Shut down a virtual machine</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

<span data-ttu-id="85651-111">Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="85651-111">This command shuts down a virtual machine that the specified service contains.</span></span>

### <span data-ttu-id="85651-112">Beispiel 2: Herunterfahren eines virtuellen Computers mit einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="85651-112">Example 2: Shut down a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

<span data-ttu-id="85651-113">Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, indem Sie das Objekt des virtuellen Computers verwenden, das von **Get-AzureVM** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="85651-113">This command shuts down a virtual machine that the specified service contains, by using the virtual machine object that **Get-AzureVM** returns.</span></span>

### <span data-ttu-id="85651-114">Beispiel 3: Herunterfahren eines virtuellen Computers und beibehalten der bereitgestellten VM</span><span class="sxs-lookup"><span data-stu-id="85651-114">Example 3: Shut down a VM and keep the VM provisioned</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

<span data-ttu-id="85651-115">Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, und hält ihn bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="85651-115">This command shuts down a virtual machine that the specified service contains, and keeps it provisioned.</span></span>

### <span data-ttu-id="85651-116">Beispiel 4: Herunterfahren eines virtuellen Computers und zulassen der Freigabe des letzten virtuellen Computers in der Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="85651-116">Example 4: Shut down a VM and allow deallocation of the last VM in the deployment</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

<span data-ttu-id="85651-117">Dieser Befehl beendet einen virtuellen Computer, den der angegebene Dienst enthält, und ermöglicht die Freigabe des letzten virtuellen Computers in der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="85651-117">This command shuts down a virtual machine that the specified service contains and allows deallocation of the last virtual machine in the deployment.</span></span>

### <span data-ttu-id="85651-118">Beispiel 5: Herunterfahren mehrerer VMS</span><span class="sxs-lookup"><span data-stu-id="85651-118">Example 5: Shut down multiple VMs</span></span>
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

<span data-ttu-id="85651-119">Mit diesem Befehl werden mehrere virtuelle Computer, die der angegebene Dienst enthält, heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="85651-119">This command shuts down multiple virtual machines that the specified service contains.</span></span>

## <span data-ttu-id="85651-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="85651-120">PARAMETERS</span></span>

### <span data-ttu-id="85651-121">-Force</span><span class="sxs-lookup"><span data-stu-id="85651-121">-Force</span></span>
<span data-ttu-id="85651-122">Gibt an, ob die Freigabe des letzten virtuellen Computers in einer Bereitstellung zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="85651-122">Specifies whether to allow the deallocation of the last virtual machine in a deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85651-123">-Information</span><span class="sxs-lookup"><span data-stu-id="85651-123">-InformationAction</span></span>
<span data-ttu-id="85651-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="85651-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="85651-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="85651-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="85651-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="85651-126">Continue</span></span>
- <span data-ttu-id="85651-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="85651-127">Ignore</span></span>
- <span data-ttu-id="85651-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="85651-128">Inquire</span></span>
- <span data-ttu-id="85651-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="85651-129">SilentlyContinue</span></span>
- <span data-ttu-id="85651-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="85651-130">Stop</span></span>
- <span data-ttu-id="85651-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="85651-131">Suspend</span></span>

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

### <span data-ttu-id="85651-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="85651-132">-InformationVariable</span></span>
<span data-ttu-id="85651-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="85651-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="85651-134">-Name</span><span class="sxs-lookup"><span data-stu-id="85651-134">-Name</span></span>
<span data-ttu-id="85651-135">Gibt den Namen des virtuellen Computers an, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85651-135">Specifies the name of the virtual machine to shut down.</span></span>

<span data-ttu-id="85651-136">Verwenden Sie das Platzhalterzeichen, um mehrere virtuelle Computer asynchron zu beenden.</span><span class="sxs-lookup"><span data-stu-id="85651-136">Use the wildcard character to stop multiple virtual machines asynchronously.</span></span>
<span data-ttu-id="85651-137">Mit einem Platzhalterzeichen ruft dieses Cmdlet die Operation Shutdown Roles https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) anstelle des Vorgangs für das Herunterfahren der Rolle https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .</span><span class="sxs-lookup"><span data-stu-id="85651-137">With a wildcard character, this cmdlet calls the Shutdown Roleshttps://msdn.microsoft.com/en-us/library/azure/dn469421.aspx operation (https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx), instead of the Shutdown Rolehttps://msdn.microsoft.com/en-us/library/azure/jj157195.aspx operation (https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx).</span></span>

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85651-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="85651-138">-Profile</span></span>
<span data-ttu-id="85651-139">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="85651-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="85651-140">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="85651-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="85651-141">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="85651-141">-ServiceName</span></span>
<span data-ttu-id="85651-142">Gibt den Namen des Azure-Diensts an, der den virtuellen Computer enthält, der beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85651-142">Specifies the name of the Azure service that contains the virtual machine to shut down.</span></span>

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

### <span data-ttu-id="85651-143">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="85651-143">-StayProvisioned</span></span>
<span data-ttu-id="85651-144">Gibt an, dass das Cmdlet die Bereitstellung des virtuellen Computers verhindert.</span><span class="sxs-lookup"><span data-stu-id="85651-144">Specifies that this cmdlet keeps the virtual machine provisioned.</span></span>

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

### <span data-ttu-id="85651-145">-VM</span><span class="sxs-lookup"><span data-stu-id="85651-145">-VM</span></span>
<span data-ttu-id="85651-146">Gibt ein Objekt eines virtuellen Computers an, das den zu beendenden virtuellen Computer identifiziert.</span><span class="sxs-lookup"><span data-stu-id="85651-146">Specifies a virtual machine object that identifies the virtual machine to shut down.</span></span>

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85651-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85651-147">CommonParameters</span></span>
<span data-ttu-id="85651-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85651-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85651-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85651-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85651-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85651-150">INPUTS</span></span>

## <span data-ttu-id="85651-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85651-151">OUTPUTS</span></span>

## <span data-ttu-id="85651-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="85651-152">NOTES</span></span>

## <span data-ttu-id="85651-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85651-153">RELATED LINKS</span></span>

[<span data-ttu-id="85651-154">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="85651-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="85651-155">Neu – AzureVM</span><span class="sxs-lookup"><span data-stu-id="85651-155">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="85651-156">Neustart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="85651-156">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="85651-157">Anfang-AzureVM</span><span class="sxs-lookup"><span data-stu-id="85651-157">Start-AzureVM</span></span>](./Start-AzureVM.md)


