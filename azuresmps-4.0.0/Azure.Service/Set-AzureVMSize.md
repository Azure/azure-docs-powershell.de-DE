---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 437889D1-F24F-4BBE-8C56-7C3E48CEA517
online version: ''
schema: 2.0.0
ms.openlocfilehash: 86dd38ce7fa55507be3362c1494b88df491a1067
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005997"
---
# <span data-ttu-id="232ef-101">Set-AzureVMSize</span><span class="sxs-lookup"><span data-stu-id="232ef-101">Set-AzureVMSize</span></span>

## <span data-ttu-id="232ef-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="232ef-102">SYNOPSIS</span></span>
<span data-ttu-id="232ef-103">Legt die Größe eines Azure Virtual Machine fest.</span><span class="sxs-lookup"><span data-stu-id="232ef-103">Sets the size of an Azure virtual machine.</span></span>

## <span data-ttu-id="232ef-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="232ef-104">SYNTAX</span></span>

```
Set-AzureVMSize [-InstanceSize] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="232ef-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="232ef-105">DESCRIPTION</span></span>
<span data-ttu-id="232ef-106">Das Cmdlet " **Satz-AzureVMSize** " aktualisiert die Größe eines virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="232ef-106">The **Set-AzureVMSize** cmdlet updates the size of a virtual machine.</span></span>
<span data-ttu-id="232ef-107">Es hat zwei Parameter: *Instanzen* , also die neue Größe des virtuellen Computers, und *VM* , bei der es sich um ein virtuelles Computerobjekt handelt, das mit dem Cmdlet **Get-AzureVM** abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="232ef-107">It has two parameters: *InstanceSize* , which is the new size of the virtual machine, and *VM* , which is a virtual machine object retrieved by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="232ef-108">Das Ergebnis von **AzureVMSize** kann an das **Update-AzureVM-** Cmdlet weitergeleitet oder zur späteren Verwendung in einer Variablen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="232ef-108">The result of **Set-AzureVMSize** can be piped to the **Update-AzureVM** cmdlet or stored in a variable for later use.</span></span>
<span data-ttu-id="232ef-109">Eine tatsächliche Änderung wird erst vorgenommen, wenn **Update-AzureVM** ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="232ef-109">No actual change is made until **Update-AzureVM** is executed.</span></span>

<span data-ttu-id="232ef-110">Hinweis: für dieses Cmdlet muss die virtuelle Maschine erneut bereitgestellt werden, und es wird möglicherweise eine neue IP-Adresse abgerufen.</span><span class="sxs-lookup"><span data-stu-id="232ef-110">Note: This cmdlet will require the virtual machine to be re-provisioned and it might get a new IP address.</span></span>

## <span data-ttu-id="232ef-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="232ef-111">EXAMPLES</span></span>

### <span data-ttu-id="232ef-112">Beispiel 1: Bestimmen der Größe eines virtuellen Computers</span><span class="sxs-lookup"><span data-stu-id="232ef-112">Example 1: Set the size of a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "MySvc1" -Name "MyVM3" | Set-AzureVMSize "Small" | Update-AzureVM
```

<span data-ttu-id="232ef-113">Dieser Befehl aktualisiert einen virtuellen Computer, um die Größe "klein" zu ändern.</span><span class="sxs-lookup"><span data-stu-id="232ef-113">This command updates a virtual machine to size "Small".</span></span>

## <span data-ttu-id="232ef-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="232ef-114">PARAMETERS</span></span>

### <span data-ttu-id="232ef-115">-Information</span><span class="sxs-lookup"><span data-stu-id="232ef-115">-InformationAction</span></span>
<span data-ttu-id="232ef-116">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="232ef-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="232ef-117">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="232ef-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="232ef-118">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="232ef-118">Continue</span></span>
- <span data-ttu-id="232ef-119">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="232ef-119">Ignore</span></span>
- <span data-ttu-id="232ef-120">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="232ef-120">Inquire</span></span>
- <span data-ttu-id="232ef-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="232ef-121">SilentlyContinue</span></span>
- <span data-ttu-id="232ef-122">Beenden</span><span class="sxs-lookup"><span data-stu-id="232ef-122">Stop</span></span>
- <span data-ttu-id="232ef-123">Anhalten</span><span class="sxs-lookup"><span data-stu-id="232ef-123">Suspend</span></span>

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

### <span data-ttu-id="232ef-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="232ef-124">-InformationVariable</span></span>
<span data-ttu-id="232ef-125">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="232ef-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="232ef-126">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="232ef-126">-InstanceSize</span></span>
<span data-ttu-id="232ef-127">Gibt die Größe des virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="232ef-127">Specifies the size of the virtual machine.</span></span>

<span data-ttu-id="232ef-128">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="232ef-128">The acceptable values for this parameter are:</span></span>

<span data-ttu-id="232ef-129">--ExtraSmall--klein--mittel--groß--extra large--A5--A6--A7</span><span class="sxs-lookup"><span data-stu-id="232ef-129">--ExtraSmall --Small --Medium --Large --ExtraLarge --A5 --A6 --A7</span></span>

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

### <span data-ttu-id="232ef-130">-Profil</span><span class="sxs-lookup"><span data-stu-id="232ef-130">-Profile</span></span>
<span data-ttu-id="232ef-131">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="232ef-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="232ef-132">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="232ef-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="232ef-133">-VM</span><span class="sxs-lookup"><span data-stu-id="232ef-133">-VM</span></span>
<span data-ttu-id="232ef-134">Gibt das Objekt des beständigen virtuellen Computers an, dessen Größe von diesem Cmdlet festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="232ef-134">Specifies the persistent virtual machine object that this cmdlet sets the size of.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="232ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="232ef-135">CommonParameters</span></span>
<span data-ttu-id="232ef-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="232ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="232ef-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="232ef-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="232ef-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="232ef-138">INPUTS</span></span>

## <span data-ttu-id="232ef-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="232ef-139">OUTPUTS</span></span>

## <span data-ttu-id="232ef-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="232ef-140">NOTES</span></span>

## <span data-ttu-id="232ef-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="232ef-141">RELATED LINKS</span></span>

[<span data-ttu-id="232ef-142">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="232ef-142">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="232ef-143">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="232ef-143">Update-AzureVM</span></span>](./Update-AzureVM.md)


