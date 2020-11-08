---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C60F78AE-3803-4D9F-A4F3-EAA42052C0E4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6a0708ca37cdb2b700772da2fe9cb684b8b29a30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005977"
---
# <span data-ttu-id="f739e-101">Start-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-101">Start-AzureVM</span></span>

## <span data-ttu-id="f739e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f739e-102">SYNOPSIS</span></span>
<span data-ttu-id="f739e-103">Startet einen virtuellen Azure-Computer.</span><span class="sxs-lookup"><span data-stu-id="f739e-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="f739e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f739e-104">SYNTAX</span></span>

### <span data-ttu-id="f739e-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f739e-105">ByName (Default)</span></span>
```
Start-AzureVM [-Name] <String[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="f739e-106">Eingabe</span><span class="sxs-lookup"><span data-stu-id="f739e-106">Input</span></span>
```
Start-AzureVM -VM <IPersistentVM[]> [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="f739e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f739e-107">DESCRIPTION</span></span>
<span data-ttu-id="f739e-108">Das Cmdlet **Start-AzureVM** fordert den Start einer virtuellen Azure-Maschine an.</span><span class="sxs-lookup"><span data-stu-id="f739e-108">The **Start-AzureVM** cmdlet requests the start of an Azure virtual machine.</span></span>

## <span data-ttu-id="f739e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f739e-109">EXAMPLES</span></span>

### <span data-ttu-id="f739e-110">Beispiel 1: Starten eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="f739e-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureVM -ServiceName "ContosoService03" -Name "VirtualMachine04"
```

<span data-ttu-id="f739e-111">Dieser Befehl startet den virtuellen Computer mit dem Namen "VirtualMachine04", der im Azure-Dienst mit dem Namen ContosoService03 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f739e-111">This command starts the virtual machine named VirtualMachine04 that runs in the Azure service named ContosoService03.</span></span>

### <span data-ttu-id="f739e-112">Beispiel 2: Starten eines virtuellen Computers mit einem virtuellen Computerobjekt</span><span class="sxs-lookup"><span data-stu-id="f739e-112">Example 2: Start a virtual machine by using a virtual machine object</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService03" -Name "DatabaseServer" | Start-AzureVM
```

<span data-ttu-id="f739e-113">Dieser Befehl ruft das Virtual Machine-Objekt für den virtuellen Computer ab, dessen Name databaseserver ist, und fordert dann an, es zu starten.</span><span class="sxs-lookup"><span data-stu-id="f739e-113">This command retrieves the virtual machine object for the virtual machine whose name is DatabaseServer, and then requests to start it.</span></span>

## <span data-ttu-id="f739e-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="f739e-114">PARAMETERS</span></span>

### <span data-ttu-id="f739e-115">-Information</span><span class="sxs-lookup"><span data-stu-id="f739e-115">-InformationAction</span></span>
<span data-ttu-id="f739e-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="f739e-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="f739e-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f739e-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f739e-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="f739e-118">Continue</span></span>
- <span data-ttu-id="f739e-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="f739e-119">Ignore</span></span>
- <span data-ttu-id="f739e-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="f739e-120">Inquire</span></span>
- <span data-ttu-id="f739e-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="f739e-121">SilentlyContinue</span></span>
- <span data-ttu-id="f739e-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="f739e-122">Stop</span></span>
- <span data-ttu-id="f739e-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="f739e-123">Suspend</span></span>

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

### <span data-ttu-id="f739e-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="f739e-124">-InformationVariable</span></span>
<span data-ttu-id="f739e-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="f739e-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="f739e-126">-Name</span><span class="sxs-lookup"><span data-stu-id="f739e-126">-Name</span></span>
<span data-ttu-id="f739e-127">Gibt den Namen der virtuellen Maschine an, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f739e-127">Specifies the name of the virtual machine to start.</span></span>

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

### <span data-ttu-id="f739e-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="f739e-128">-Profile</span></span>
<span data-ttu-id="f739e-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f739e-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f739e-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f739e-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f739e-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f739e-131">-ServiceName</span></span>
<span data-ttu-id="f739e-132">Gibt den Namen des Azure-Diensts an, der den virtuellen Computer enthält, der gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f739e-132">Specifies the name of the Azure service that contains the virtual machine to start.</span></span>

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

### <span data-ttu-id="f739e-133">-VM</span><span class="sxs-lookup"><span data-stu-id="f739e-133">-VM</span></span>
<span data-ttu-id="f739e-134">Gibt ein Objekt eines virtuellen Computers an, das den Start des virtuellen Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="f739e-134">Specifies a virtual machine object that identifies the virtual machine to start.</span></span>

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

### <span data-ttu-id="f739e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f739e-135">CommonParameters</span></span>
<span data-ttu-id="f739e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f739e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f739e-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f739e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f739e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f739e-138">INPUTS</span></span>

## <span data-ttu-id="f739e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f739e-139">OUTPUTS</span></span>

## <span data-ttu-id="f739e-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="f739e-140">NOTES</span></span>

## <span data-ttu-id="f739e-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f739e-141">RELATED LINKS</span></span>

[<span data-ttu-id="f739e-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="f739e-143">Remove-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-143">Remove-AzureVM</span></span>](./Remove-AzureVM.md)

[<span data-ttu-id="f739e-144">Neustart-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-144">Restart-AzureVM</span></span>](./Restart-AzureVM.md)

[<span data-ttu-id="f739e-145">Stopp-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-145">Stop-AzureVM</span></span>](./Stop-AzureVM.md)

[<span data-ttu-id="f739e-146">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="f739e-146">Update-AzureVM</span></span>](./Update-AzureVM.md)


