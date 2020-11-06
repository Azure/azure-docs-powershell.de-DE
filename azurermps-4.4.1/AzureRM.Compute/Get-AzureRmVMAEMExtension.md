---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 10874ffbb0846765bfbeae06ae4522989280e428
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479902"
---
# <span data-ttu-id="08caf-101">Get-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="08caf-101">Get-AzureRmVMAEMExtension</span></span>

## <span data-ttu-id="08caf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08caf-102">SYNOPSIS</span></span>
<span data-ttu-id="08caf-103">Ruft Informationen zur AEM-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="08caf-103">Gets information about the AEM extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="08caf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08caf-104">SYNTAX</span></span>

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08caf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08caf-105">DESCRIPTION</span></span>
<span data-ttu-id="08caf-106">Das Cmdlet " **Get-AzureRmVMAEMExtension** " Ruft Informationen zur Azure Enhanced Monitoring (AEM)-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="08caf-106">The **Get-AzureRmVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="08caf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08caf-107">EXAMPLES</span></span>

### <span data-ttu-id="08caf-108">Beispiel 1: Abrufen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="08caf-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="08caf-109">Dieser Befehl ruft Informationen für die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server ab.</span><span class="sxs-lookup"><span data-stu-id="08caf-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="08caf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="08caf-110">PARAMETERS</span></span>

### <span data-ttu-id="08caf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08caf-111">-DefaultProfile</span></span>
<span data-ttu-id="08caf-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08caf-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-113">-Name</span><span class="sxs-lookup"><span data-stu-id="08caf-113">-Name</span></span>
<span data-ttu-id="08caf-114">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="08caf-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="08caf-115">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="08caf-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="08caf-116">-OSType</span></span>
<span data-ttu-id="08caf-117">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="08caf-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="08caf-118">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="08caf-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="08caf-119">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="08caf-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08caf-120">-ResourceGroupName</span></span>
<span data-ttu-id="08caf-121">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="08caf-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="08caf-122">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="08caf-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-123">-Status</span><span class="sxs-lookup"><span data-stu-id="08caf-123">-Status</span></span>
<span data-ttu-id="08caf-124">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der AEM-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="08caf-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="08caf-125">-VMName</span></span>
<span data-ttu-id="08caf-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="08caf-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="08caf-127">Dieses Cmdlet ruft Informationen zur AEM-Erweiterung für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="08caf-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08caf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08caf-128">CommonParameters</span></span>
<span data-ttu-id="08caf-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08caf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08caf-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08caf-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08caf-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08caf-131">INPUTS</span></span>

## <span data-ttu-id="08caf-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08caf-132">OUTPUTS</span></span>

## <span data-ttu-id="08caf-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="08caf-133">NOTES</span></span>

## <span data-ttu-id="08caf-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08caf-134">RELATED LINKS</span></span>

[<span data-ttu-id="08caf-135">Remove-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="08caf-135">Remove-AzureRmVMAEMExtension</span></span>](./Remove-AzureRmVMAEMExtension.md)

[<span data-ttu-id="08caf-136">Satz-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="08caf-136">Set-AzureRmVMAEMExtension</span></span>](./Set-AzureRmVMAEMExtension.md)

[<span data-ttu-id="08caf-137">Test-AzureRmVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="08caf-137">Test-AzureRmVMAEMExtension</span></span>](./Test-AzureRmVMAEMExtension.md)


