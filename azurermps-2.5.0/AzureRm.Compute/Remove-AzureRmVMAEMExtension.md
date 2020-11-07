---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B1CD5302-9BF0-460E-98FE-F60DFE072848
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmaemextension
schema: 2.0.0
ms.openlocfilehash: cf70191c47f3778268b0087ea542a6812155ebbb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850064"
---
# <span data-ttu-id="a47c9-101">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a47c9-101">Remove-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="a47c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a47c9-102">SYNOPSIS</span></span>
<span data-ttu-id="a47c9-103">Entfernt die AEM-Erweiterung von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a47c9-103">Removes the AEM extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a47c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a47c9-104">SYNTAX</span></span>

```
Remove-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a47c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a47c9-105">DESCRIPTION</span></span>
<span data-ttu-id="a47c9-106">Das Cmdlet **Remove-AzureRmVMAEMExtension** entfernt die Erweiterung Azure Enhanced Monitoring (AEM) von einem virtuellen Computer.</span><span class="sxs-lookup"><span data-stu-id="a47c9-106">The **Remove-AzureRmVMAEMExtension** cmdlet removes the Azure Enhanced Monitoring (AEM) extension from a virtual machine.</span></span>

## <span data-ttu-id="a47c9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a47c9-107">EXAMPLES</span></span>

### <span data-ttu-id="a47c9-108">Beispiel 1: Entfernen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="a47c9-108">Example 1: Remove the AEM extension</span></span>
```
PS C:\> Remove-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="a47c9-109">Dieser Befehl entfernt die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server.</span><span class="sxs-lookup"><span data-stu-id="a47c9-109">This command removes the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="a47c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a47c9-110">PARAMETERS</span></span>

### <span data-ttu-id="a47c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a47c9-111">-DefaultProfile</span></span>
<span data-ttu-id="a47c9-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a47c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a47c9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a47c9-113">-Name</span></span>
<span data-ttu-id="a47c9-114">Gibt den Namen des virtuellen Computers an, von dem dieses Cmdlet die AEM-Erweiterung entfernt.</span><span class="sxs-lookup"><span data-stu-id="a47c9-114">Specifies the name of the virtual machine from which this cmdlet removes the AEM extension.</span></span>

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

### <span data-ttu-id="a47c9-115">-OSType</span><span class="sxs-lookup"><span data-stu-id="a47c9-115">-OSType</span></span>
<span data-ttu-id="a47c9-116">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="a47c9-116">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="a47c9-117">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="a47c9-117">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="a47c9-118">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="a47c9-118">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="a47c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a47c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="a47c9-120">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a47c9-120">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="a47c9-121">Dieses Cmdlet entfernt die AEM-Erweiterung von dieser virtuellen Maschine.</span><span class="sxs-lookup"><span data-stu-id="a47c9-121">This cmdlet removes the AEM extension from that virtual machine.</span></span>

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

### <span data-ttu-id="a47c9-122">-VMName</span><span class="sxs-lookup"><span data-stu-id="a47c9-122">-VMName</span></span>
<span data-ttu-id="a47c9-123">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a47c9-123">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="a47c9-124">Dieses Cmdlet entfernt die AEM-Erweiterung für den virtuellen Computer, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="a47c9-124">This cmdlet removes the AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="a47c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a47c9-125">CommonParameters</span></span>
<span data-ttu-id="a47c9-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a47c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a47c9-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a47c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a47c9-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a47c9-128">INPUTS</span></span>

### <span data-ttu-id="a47c9-129">Keine</span><span class="sxs-lookup"><span data-stu-id="a47c9-129">None</span></span>
<span data-ttu-id="a47c9-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a47c9-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a47c9-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a47c9-131">OUTPUTS</span></span>

### <span data-ttu-id="a47c9-132">Microsoft. Azure. Commands. Compute. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a47c9-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a47c9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a47c9-133">NOTES</span></span>

## <span data-ttu-id="a47c9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a47c9-134">RELATED LINKS</span></span>

[<span data-ttu-id="a47c9-135">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a47c9-135">Get-AzureRmVMAEMExtension</span></span>](./Get-AzureRmVMAEMExtension.md)

[<span data-ttu-id="a47c9-136">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a47c9-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="a47c9-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="a47c9-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


