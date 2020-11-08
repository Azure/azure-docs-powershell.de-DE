---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 19A87B24-C5A6-4505-BB54-973B24BCC68E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 821927fc465ed5af048a2f27ed84da8c12b9caa5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006742"
---
# <span data-ttu-id="addb3-101">Get-AzureVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="addb3-101">Get-AzureVMDscExtensionStatus</span></span>

## <span data-ttu-id="addb3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="addb3-102">SYNOPSIS</span></span>
<span data-ttu-id="addb3-103">Ruft den Status der DSC-Erweiterung für alle virtuellen Computer ab, die in einem clouddienst oder für einen bestimmten virtuellen Computer im Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="addb3-103">Gets the DSC extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="addb3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="addb3-104">SYNTAX</span></span>

### <span data-ttu-id="addb3-105">GetStatusByServiceAndVMName (Standard)</span><span class="sxs-lookup"><span data-stu-id="addb3-105">GetStatusByServiceAndVMName (Default)</span></span>
```
Get-AzureVMDscExtensionStatus [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="addb3-106">GetStatusByVM</span><span class="sxs-lookup"><span data-stu-id="addb3-106">GetStatusByVM</span></span>
```
Get-AzureVMDscExtensionStatus -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="addb3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="addb3-107">DESCRIPTION</span></span>
<span data-ttu-id="addb3-108">Das Cmdlet " **Get-AzureVMDscExtensionStatus** " Ruft den Status der gewünschten Statuskonfiguration (DSC) für alle virtuellen Computer ab, die in einem clouddienst oder für einen bestimmten virtuellen Computer im Dienst bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="addb3-108">The **Get-AzureVMDscExtensionStatus** cmdlet gets the Desired State Configuration (DSC) extension status for all the virtual machines deployed in a cloud service or for a particular virtual machine in the service.</span></span>

## <span data-ttu-id="addb3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="addb3-109">EXAMPLES</span></span>

### <span data-ttu-id="addb3-110">1:</span><span class="sxs-lookup"><span data-stu-id="addb3-110">1:</span></span>
```

```

## <span data-ttu-id="addb3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="addb3-111">PARAMETERS</span></span>

### <span data-ttu-id="addb3-112">-Information</span><span class="sxs-lookup"><span data-stu-id="addb3-112">-InformationAction</span></span>
<span data-ttu-id="addb3-113">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="addb3-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="addb3-114">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="addb3-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="addb3-115">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="addb3-115">Continue</span></span>
- <span data-ttu-id="addb3-116">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="addb3-116">Ignore</span></span>
- <span data-ttu-id="addb3-117">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="addb3-117">Inquire</span></span>
- <span data-ttu-id="addb3-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="addb3-118">SilentlyContinue</span></span>
- <span data-ttu-id="addb3-119">Beenden</span><span class="sxs-lookup"><span data-stu-id="addb3-119">Stop</span></span>
- <span data-ttu-id="addb3-120">Anhalten</span><span class="sxs-lookup"><span data-stu-id="addb3-120">Suspend</span></span>

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

### <span data-ttu-id="addb3-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="addb3-121">-InformationVariable</span></span>
<span data-ttu-id="addb3-122">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="addb3-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="addb3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="addb3-123">-Name</span></span>
<span data-ttu-id="addb3-124">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="addb3-124">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addb3-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="addb3-125">-Profile</span></span>
<span data-ttu-id="addb3-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="addb3-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="addb3-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="addb3-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="addb3-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="addb3-128">-ServiceName</span></span>
<span data-ttu-id="addb3-129">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="addb3-129">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: GetStatusByServiceAndVMName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="addb3-130">-VM</span><span class="sxs-lookup"><span data-stu-id="addb3-130">-VM</span></span>
<span data-ttu-id="addb3-131">Gibt das Objekt des beständigen virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="addb3-131">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: GetStatusByVM
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="addb3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="addb3-132">CommonParameters</span></span>
<span data-ttu-id="addb3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="addb3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="addb3-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="addb3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="addb3-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="addb3-135">INPUTS</span></span>

## <span data-ttu-id="addb3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="addb3-136">OUTPUTS</span></span>

### <span data-ttu-id="addb3-137">Microsoft. WindowsAzure. Commands. Servicemanagement. IaaS. Extensions. VirtualMachineDscExtensionStatusContext</span><span class="sxs-lookup"><span data-stu-id="addb3-137">Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.VirtualMachineDscExtensionStatusContext</span></span>

## <span data-ttu-id="addb3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="addb3-138">NOTES</span></span>

## <span data-ttu-id="addb3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="addb3-139">RELATED LINKS</span></span>

[<span data-ttu-id="addb3-140">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="addb3-140">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="addb3-141">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="addb3-141">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="addb3-142">Satz-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="addb3-142">Set-AzureVMDscExtension</span></span>](./Set-AzureVMDscExtension.md)


