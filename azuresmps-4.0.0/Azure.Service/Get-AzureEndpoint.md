---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1CFB90FD-7BC5-4687-8D08-775097DDA062
online version: ''
schema: 2.0.0
ms.openlocfilehash: 651b38a21dff03ce3c5925040d65bc2967eeaa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005851"
---
# <span data-ttu-id="606b4-101">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="606b4-101">Get-AzureEndpoint</span></span>

## <span data-ttu-id="606b4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="606b4-102">SYNOPSIS</span></span>
<span data-ttu-id="606b4-103">Ruft Informationen zu den Endpunkten ab, die einem Azure Virtual Machine zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="606b4-103">Gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="606b4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="606b4-104">SYNTAX</span></span>

```
Get-AzureEndpoint [[-Name] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="606b4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="606b4-105">DESCRIPTION</span></span>
<span data-ttu-id="606b4-106">Das Cmdlet " **Get-AzureEndpoint** " Ruft Informationen zu den Endpunkten ab, die einem Azure Virtual Machine zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="606b4-106">The **Get-AzureEndpoint** cmdlet gets information about the endpoints that are assigned to an Azure virtual machine.</span></span>

## <span data-ttu-id="606b4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="606b4-107">EXAMPLES</span></span>

### <span data-ttu-id="606b4-108">Beispiel 1: Abrufen von Endpunktinformationen für einen virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="606b4-108">Example 1: Get endpoint information for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine12" | Get-AzureEndpoint
```

<span data-ttu-id="606b4-109">Dieser Befehl ruft mit dem Cmdlet **Get-AzureVM** die Konfiguration eines virtuellen Computers mit dem Namen VirtualMachine12 ab.</span><span class="sxs-lookup"><span data-stu-id="606b4-109">This command retrieves the configuration of a virtual machine named VirtualMachine12 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="606b4-110">Der Befehl übergibt ihn mithilfe des Pipelineoperators an das aktuelle Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="606b4-110">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="606b4-111">Dieses Cmdlet ruft Endpunktinformationen für diesen virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="606b4-111">This cmdlet gets endpoint information for that virtual machine.</span></span>

## <span data-ttu-id="606b4-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="606b4-112">PARAMETERS</span></span>

### <span data-ttu-id="606b4-113">-Information</span><span class="sxs-lookup"><span data-stu-id="606b4-113">-InformationAction</span></span>
<span data-ttu-id="606b4-114">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="606b4-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="606b4-115">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="606b4-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="606b4-116">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="606b4-116">Continue</span></span>
- <span data-ttu-id="606b4-117">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="606b4-117">Ignore</span></span>
- <span data-ttu-id="606b4-118">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="606b4-118">Inquire</span></span>
- <span data-ttu-id="606b4-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="606b4-119">SilentlyContinue</span></span>
- <span data-ttu-id="606b4-120">Beenden</span><span class="sxs-lookup"><span data-stu-id="606b4-120">Stop</span></span>
- <span data-ttu-id="606b4-121">Anhalten</span><span class="sxs-lookup"><span data-stu-id="606b4-121">Suspend</span></span>

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

### <span data-ttu-id="606b4-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="606b4-122">-InformationVariable</span></span>
<span data-ttu-id="606b4-123">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="606b4-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="606b4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="606b4-124">-Name</span></span>
<span data-ttu-id="606b4-125">Gibt den Namen des Endpunkts an, für den dieses Cmdlet Informationen erhält.</span><span class="sxs-lookup"><span data-stu-id="606b4-125">Specifies the name of the endpoint for which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="606b4-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="606b4-126">-Profile</span></span>
<span data-ttu-id="606b4-127">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="606b4-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="606b4-128">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="606b4-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="606b4-129">-VM</span><span class="sxs-lookup"><span data-stu-id="606b4-129">-VM</span></span>
<span data-ttu-id="606b4-130">Gibt den virtuellen Computer an, von dem dieses Cmdlet Endpunktinformationen erhält.</span><span class="sxs-lookup"><span data-stu-id="606b4-130">Specifies the virtual machine from which this cmdlet gets endpoint information.</span></span>

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

### <span data-ttu-id="606b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="606b4-131">CommonParameters</span></span>
<span data-ttu-id="606b4-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="606b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="606b4-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="606b4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="606b4-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="606b4-134">INPUTS</span></span>

## <span data-ttu-id="606b4-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="606b4-135">OUTPUTS</span></span>

## <span data-ttu-id="606b4-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="606b4-136">NOTES</span></span>

## <span data-ttu-id="606b4-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="606b4-137">RELATED LINKS</span></span>

[<span data-ttu-id="606b4-138">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="606b4-138">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="606b4-139">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="606b4-139">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="606b4-140">Remove-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="606b4-140">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="606b4-141">Satz-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="606b4-141">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)


