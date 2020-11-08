---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaemextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAEMExtension.md
ms.openlocfilehash: 0879458284c7e08b2e8371b9b8d8b894a482a9df
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008643"
---
# <span data-ttu-id="28a94-101">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="28a94-101">Get-AzVMAEMExtension</span></span>

## <span data-ttu-id="28a94-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28a94-102">SYNOPSIS</span></span>
<span data-ttu-id="28a94-103">Ruft Informationen zur AEM-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="28a94-103">Gets information about the AEM extension.</span></span>

## <span data-ttu-id="28a94-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28a94-104">SYNTAX</span></span>

```
Get-AzVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28a94-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28a94-105">DESCRIPTION</span></span>
<span data-ttu-id="28a94-106">Das Cmdlet " **Get-AzVMAEMExtension** " Ruft Informationen zur Azure Enhanced Monitoring (AEM)-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="28a94-106">The **Get-AzVMAEMExtension** cmdlet gets information about the Azure Enhanced Monitoring (AEM) extension.</span></span>

## <span data-ttu-id="28a94-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28a94-107">EXAMPLES</span></span>

### <span data-ttu-id="28a94-108">Beispiel 1: Abrufen der AEM-Erweiterung</span><span class="sxs-lookup"><span data-stu-id="28a94-108">Example 1: Get the AEM extension</span></span>
```
PS C:\> Get-AzVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

<span data-ttu-id="28a94-109">Dieser Befehl ruft Informationen für die AEM-Erweiterung für den virtuellen Computer mit dem Namen Contoso-Server ab.</span><span class="sxs-lookup"><span data-stu-id="28a94-109">This command gets information for the AEM extension for the virtual machine named contoso-server.</span></span>

## <span data-ttu-id="28a94-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="28a94-110">PARAMETERS</span></span>

### <span data-ttu-id="28a94-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28a94-111">-DefaultProfile</span></span>
<span data-ttu-id="28a94-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28a94-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28a94-113">-Name</span><span class="sxs-lookup"><span data-stu-id="28a94-113">-Name</span></span>
<span data-ttu-id="28a94-114">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="28a94-114">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="28a94-115">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab, die von diesem Cmdlet angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="28a94-115">This cmdlet gets information for the AEM extension on the virtual machine that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="28a94-116">-OSType</span><span class="sxs-lookup"><span data-stu-id="28a94-116">-OSType</span></span>
<span data-ttu-id="28a94-117">Gibt den Typ des Betriebssystems des Betriebssystemdatenträgers an.</span><span class="sxs-lookup"><span data-stu-id="28a94-117">Specifies the type of the operating system of the operating system disk.</span></span>
<span data-ttu-id="28a94-118">Wenn auf dem Betriebssystemdatenträger kein Typ vorhanden ist, müssen Sie diesen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="28a94-118">If the operating system disk does not have a type, you must specify this parameter.</span></span>
<span data-ttu-id="28a94-119">Die akzeptablen Werte für diesen Parameter sind: Windows und Linux.</span><span class="sxs-lookup"><span data-stu-id="28a94-119">The acceptable values for this parameter are: Windows and Linux.</span></span>

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

### <span data-ttu-id="28a94-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28a94-120">-ResourceGroupName</span></span>
<span data-ttu-id="28a94-121">Gibt den Namen der Ressourcengruppe einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="28a94-121">Specifies the name of the resource group of a virtual machine.</span></span>
<span data-ttu-id="28a94-122">Dieses Cmdlet ruft Informationen für die AEM-Erweiterung auf dem virtuellen Computer ab.</span><span class="sxs-lookup"><span data-stu-id="28a94-122">This cmdlet gets information for the AEM extension on that virtual machine.</span></span>

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

### <span data-ttu-id="28a94-123">-Status</span><span class="sxs-lookup"><span data-stu-id="28a94-123">-Status</span></span>
<span data-ttu-id="28a94-124">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der AEM-Erweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="28a94-124">Indicates that this cmdlet gets only the instance view of the AEM extension.</span></span>

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

### <span data-ttu-id="28a94-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="28a94-125">-VMName</span></span>
<span data-ttu-id="28a94-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="28a94-126">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="28a94-127">Dieses Cmdlet ruft Informationen zur AEM-Erweiterung für den virtuellen Computer ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="28a94-127">This cmdlet gets information about AEM extension for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="28a94-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28a94-128">CommonParameters</span></span>
<span data-ttu-id="28a94-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28a94-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28a94-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28a94-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28a94-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28a94-131">INPUTS</span></span>

### <span data-ttu-id="28a94-132">System. String</span><span class="sxs-lookup"><span data-stu-id="28a94-132">System.String</span></span>

### <span data-ttu-id="28a94-133">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="28a94-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="28a94-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28a94-134">OUTPUTS</span></span>

### <span data-ttu-id="28a94-135">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="28a94-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="28a94-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="28a94-136">NOTES</span></span>

## <span data-ttu-id="28a94-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28a94-137">RELATED LINKS</span></span>

[<span data-ttu-id="28a94-138">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="28a94-138">Remove-AzVMAEMExtension</span></span>](./Remove-AzVMAEMExtension.md)

[<span data-ttu-id="28a94-139">Satz-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="28a94-139">Set-AzVMAEMExtension</span></span>](./Set-AzVMAEMExtension.md)

[<span data-ttu-id="28a94-140">Test-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="28a94-140">Test-AzVMAEMExtension</span></span>](./Test-AzVMAEMExtension.md)


