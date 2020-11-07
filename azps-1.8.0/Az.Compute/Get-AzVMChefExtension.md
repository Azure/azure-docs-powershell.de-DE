---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: 0e04339fb9f3be8f63fc928f0bd904f80d59225b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661556"
---
# <span data-ttu-id="83fc9-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="83fc9-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="83fc9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="83fc9-102">SYNOPSIS</span></span>
<span data-ttu-id="83fc9-103">Ruft Informationen zur Erweiterung des Chefkochs ab.</span><span class="sxs-lookup"><span data-stu-id="83fc9-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="83fc9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="83fc9-104">SYNTAX</span></span>

### <span data-ttu-id="83fc9-105">Linux</span><span class="sxs-lookup"><span data-stu-id="83fc9-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83fc9-106">Windows</span><span class="sxs-lookup"><span data-stu-id="83fc9-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83fc9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83fc9-107">DESCRIPTION</span></span>
<span data-ttu-id="83fc9-108">Das Cmdlet " **Get-AzVMChefExtension** " Ruft Informationen zu einer auf einem virtuellen Computer installierten Chefkoch-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="83fc9-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="83fc9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83fc9-109">EXAMPLES</span></span>

### <span data-ttu-id="83fc9-110">Beispiel 1: Abrufen der Details der Erweiterung "Chef" für einen virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="83fc9-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="83fc9-111">Dieser Befehl ruft die Erweiterung des Chefkochs von einem Windows-virtuellen Computer mit dem Namen WindowsVM001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup001 gehört.</span><span class="sxs-lookup"><span data-stu-id="83fc9-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="83fc9-112">Beispiel 2: Abrufen der Details der Erweiterung "Chef" für einen virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="83fc9-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="83fc9-113">Dieser Befehl ruft die Erweiterung des Chefkochs von einem virtuellen Linux-Computer mit dem Namen LinuxVM001 ab, der zur Ressourcengruppe mit dem Namen ResourceGroup002 gehört.</span><span class="sxs-lookup"><span data-stu-id="83fc9-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="83fc9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="83fc9-114">PARAMETERS</span></span>

### <span data-ttu-id="83fc9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fc9-115">-DefaultProfile</span></span>
<span data-ttu-id="83fc9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="83fc9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83fc9-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="83fc9-117">-Linux</span></span>
<span data-ttu-id="83fc9-118">Gibt an, dass dieses Cmdlet auf einem virtuellen Linux-Computer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="83fc9-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fc9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="83fc9-119">-Name</span></span>
<span data-ttu-id="83fc9-120">Gibt den Namen der Erweiterung "Chef" an.</span><span class="sxs-lookup"><span data-stu-id="83fc9-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="83fc9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83fc9-121">-ResourceGroupName</span></span>
<span data-ttu-id="83fc9-122">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="83fc9-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="83fc9-123">-Status</span><span class="sxs-lookup"><span data-stu-id="83fc9-123">-Status</span></span>
<span data-ttu-id="83fc9-124">Gibt an, dass dieses Cmdlet nur die Instanzen Ansicht der Erweiterung "Chef" erhält.</span><span class="sxs-lookup"><span data-stu-id="83fc9-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="83fc9-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="83fc9-125">-VMName</span></span>
<span data-ttu-id="83fc9-126">Gibt den Namen einer virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="83fc9-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="83fc9-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="83fc9-127">-Windows</span></span>
<span data-ttu-id="83fc9-128">Gibt an, dass dieses Cmdlet für einen virtuellen Windows-Computer gilt.</span><span class="sxs-lookup"><span data-stu-id="83fc9-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83fc9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fc9-129">CommonParameters</span></span>
<span data-ttu-id="83fc9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83fc9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fc9-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83fc9-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fc9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="83fc9-132">INPUTS</span></span>

### <span data-ttu-id="83fc9-133">System. String</span><span class="sxs-lookup"><span data-stu-id="83fc9-133">System.String</span></span>

### <span data-ttu-id="83fc9-134">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="83fc9-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="83fc9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="83fc9-135">OUTPUTS</span></span>

### <span data-ttu-id="83fc9-136">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="83fc9-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="83fc9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="83fc9-137">NOTES</span></span>

## <span data-ttu-id="83fc9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="83fc9-138">RELATED LINKS</span></span>

[<span data-ttu-id="83fc9-139">Satz-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="83fc9-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="83fc9-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="83fc9-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


