---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMAEMExtension.md
ms.openlocfilehash: fb31bffbdb61c42ea1388c85b71f26af69056c54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483093"
---
# <span data-ttu-id="e4596-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e4596-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="e4596-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e4596-102">SYNOPSIS</span></span>
<span data-ttu-id="e4596-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e4596-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4596-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4596-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [<CommonParameters>]
```

## <span data-ttu-id="e4596-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e4596-105">DESCRIPTION</span></span>
<span data-ttu-id="e4596-106">Das Cmdlet **Remove-AzureRmVMAEMExtension** entfernt die Erweiterung Azure Enhanced Monitoring (AEM) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="e4596-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="e4596-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e4596-107">EXAMPLES</span></span>

### <span data-ttu-id="e4596-108">Beispiel 1: Entfernen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="e4596-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="e4596-109">Dieser Befehl entfernt die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="e4596-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="e4596-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e4596-110">PARAMETERS</span></span>

### <span data-ttu-id="e4596-111">-Name</span><span class="sxs-lookup"><span data-stu-id="e4596-111">-Name</span></span>
<span data-ttu-id="e4596-112">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die AEM-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="e4596-112">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="e4596-113">-OSType</span><span class="sxs-lookup"><span data-stu-id="e4596-113">-OSType</span></span>
<span data-ttu-id="e4596-114">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="e4596-114">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="e4596-115">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="e4596-115">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="e4596-116">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="e4596-116">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4596-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4596-117">-ResourceGroupName</span></span>
<span data-ttu-id="e4596-118">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="e4596-118">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="e4596-119">Dieses Cmdlet entfernt die AEM-Erweiterung von dieser virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="e4596-119">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="e4596-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="e4596-120">-VMName</span></span>
<span data-ttu-id="e4596-121">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="e4596-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="e4596-122">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="e4596-122">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4596-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4596-123">CommonParameters</span></span>
<span data-ttu-id="e4596-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4596-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4596-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4596-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4596-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e4596-126">INPUTS</span></span>

### <span data-ttu-id="e4596-127">Keine</span><span class="sxs-lookup"><span data-stu-id="e4596-127">None</span></span>
<span data-ttu-id="e4596-128">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="e4596-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4596-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e4596-129">OUTPUTS</span></span>

## <span data-ttu-id="e4596-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="e4596-130">NOTES</span></span>

## <span data-ttu-id="e4596-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e4596-131">RELATED LINKS</span></span>

[<span data-ttu-id="e4596-132">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e4596-132">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="e4596-133">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e4596-133">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="e4596-134">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="e4596-134">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


