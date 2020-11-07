---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664688"
---
# <span data-ttu-id="7f09b-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7f09b-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="7f09b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f09b-102">SYNOPSIS</span></span>
<span data-ttu-id="7f09b-103">Ruft Informationen zur AEM-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="7f09b-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f09b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f09b-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="7f09b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f09b-105">DESCRIPTION</span></span>
<span data-ttu-id="7f09b-106">Das Cmdlet " **Get-AzureRmVMAEMExtension** " Ruft Informationen zur Azure Enhanced Monitoring (AEM)-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="7f09b-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="7f09b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f09b-107">EXAMPLES</span></span>

### <span data-ttu-id="7f09b-108">Beispiel 1: Abrufen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="7f09b-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="7f09b-109">Dieser Befehl ruft Informationen für die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server ab.</span><span class="sxs-lookup"><span data-stu-id="7f09b-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="7f09b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f09b-110">PARAMETERS</span></span>

### <span data-ttu-id="7f09b-111">-Name</span><span class="sxs-lookup"><span data-stu-id="7f09b-111">-Name</span></span>
<span data-ttu-id="7f09b-112">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7f09b-112">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7f09b-113">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7f09b-113">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f09b-114">-OSType</span><span class="sxs-lookup"><span data-stu-id="7f09b-114">-OSType</span></span>
<span data-ttu-id="7f09b-115">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="7f09b-115">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="7f09b-116">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="7f09b-116">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="7f09b-117">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="7f09b-117">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f09b-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f09b-118">-ResourceGroupName</span></span>
<span data-ttu-id="7f09b-119">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7f09b-119">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="7f09b-120">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="7f09b-120">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="7f09b-121">-Status</span><span class="sxs-lookup"><span data-stu-id="7f09b-121">-Status</span></span>
<span data-ttu-id="7f09b-122">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der AEM-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="7f09b-122">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f09b-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f09b-123">-VMName</span></span>
<span data-ttu-id="7f09b-124">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="7f09b-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="7f09b-125">Dieses Cmdlet ruft Informationen zur AEM-Erweiterung für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="7f09b-125">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f09b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f09b-126">CommonParameters</span></span>
<span data-ttu-id="7f09b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f09b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f09b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f09b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f09b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f09b-129">INPUTS</span></span>

### <span data-ttu-id="7f09b-130">Keine</span><span class="sxs-lookup"><span data-stu-id="7f09b-130">None</span></span>
<span data-ttu-id="7f09b-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7f09b-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7f09b-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f09b-132">OUTPUTS</span></span>

## <span data-ttu-id="7f09b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f09b-133">NOTES</span></span>

## <span data-ttu-id="7f09b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f09b-134">RELATED LINKS</span></span>

[<span data-ttu-id="7f09b-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7f09b-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7f09b-136">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7f09b-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="7f09b-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="7f09b-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


