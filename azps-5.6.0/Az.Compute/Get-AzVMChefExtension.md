---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: F41953F1-9515-4081-8624-6A1494DA4BB2
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmchefextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMChefExtension.md
ms.openlocfilehash: c0d672636d273bcd6e1d2c5f3ebc1c3b70a7b208
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949544"
---
# <span data-ttu-id="97a83-101">Get-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="97a83-101">Get-AzVMChefExtension</span></span>

## <span data-ttu-id="97a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a83-102">SYNOPSIS</span></span>
<span data-ttu-id="97a83-103">Ruft Informationen zu einer Cheferweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="97a83-103">Gets information about a Chef extension.</span></span>

## <span data-ttu-id="97a83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97a83-104">SYNTAX</span></span>

### <span data-ttu-id="97a83-105">Linux</span><span class="sxs-lookup"><span data-stu-id="97a83-105">Linux</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Linux]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97a83-106">Windows</span><span class="sxs-lookup"><span data-stu-id="97a83-106">Windows</span></span>
```
Get-AzVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status] [-Windows]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a83-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="97a83-107">DESCRIPTION</span></span>
<span data-ttu-id="97a83-108">Das **Get-AzVMChefExtension-Cmdlet** ruft Informationen zu einer auf einem virtuellen Computer installierten Chef-Erweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="97a83-108">The **Get-AzVMChefExtension** cmdlet gets information about a Chef extension installed on a virtual machine.</span></span>

## <span data-ttu-id="97a83-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="97a83-109">EXAMPLES</span></span>

### <span data-ttu-id="97a83-110">Beispiel 1: Anzeigen der Details der Erweiterung "Chef" für einen virtuellen Windows-Computer</span><span class="sxs-lookup"><span data-stu-id="97a83-110">Example 1: Get the details of Chef extension for a Windows virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -Windows
```

<span data-ttu-id="97a83-111">Dieser Befehl ruft die Chef-Erweiterung von einem virtuellen Windows-Computer namens WindowsVM001 ab, der zur Ressourcengruppe "ResourceGroup001" gehört.</span><span class="sxs-lookup"><span data-stu-id="97a83-111">This command gets the Chef extension from a Windows virtual machine named WindowsVM001 that belongs to the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="97a83-112">Beispiel 2: Details zur Erweiterung "Chef" für einen virtuellen Linux-Computer</span><span class="sxs-lookup"><span data-stu-id="97a83-112">Example 2: Get the details of Chef extension for a Linux virtual machine</span></span>
```
PS C:\> Get-AzVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -Linux
```

<span data-ttu-id="97a83-113">Dieser Befehl ruft die Chef-Erweiterung von einem virtuellen Linux-Computer namens LinuxVM001 ab, der zur Ressourcengruppe "ResourceGroup002" gehört.</span><span class="sxs-lookup"><span data-stu-id="97a83-113">This command gets the Chef extension from a Linux virtual machine named LinuxVM001 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="97a83-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="97a83-114">PARAMETERS</span></span>

### <span data-ttu-id="97a83-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a83-115">-DefaultProfile</span></span>
<span data-ttu-id="97a83-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97a83-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a83-117">-Linux</span><span class="sxs-lookup"><span data-stu-id="97a83-117">-Linux</span></span>
<span data-ttu-id="97a83-118">Gibt an, dass dieses Cmdlet auf einem virtuellen Linux-Computer funktioniert.</span><span class="sxs-lookup"><span data-stu-id="97a83-118">Indicates that this cmdlet works on a Linux virtual machine.</span></span>

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

### <span data-ttu-id="97a83-119">-Name</span><span class="sxs-lookup"><span data-stu-id="97a83-119">-Name</span></span>
<span data-ttu-id="97a83-120">Gibt den Namen der Cheferweiterung an.</span><span class="sxs-lookup"><span data-stu-id="97a83-120">Specifies the name of the Chef extension.</span></span>

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

### <span data-ttu-id="97a83-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97a83-121">-ResourceGroupName</span></span>
<span data-ttu-id="97a83-122">Gibt den Namen der Ressourcengruppe an, die den virtuellen Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="97a83-122">Specifies the name of the resource group that contains the virtual machine.</span></span>

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

### <span data-ttu-id="97a83-123">-Status</span><span class="sxs-lookup"><span data-stu-id="97a83-123">-Status</span></span>
<span data-ttu-id="97a83-124">Gibt an, dass dieses Cmdlet nur die Instanzansicht der Cheferweiterung erhält.</span><span class="sxs-lookup"><span data-stu-id="97a83-124">Indicates that this cmdlet gets only the instance view of the Chef extension.</span></span>

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

### <span data-ttu-id="97a83-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="97a83-125">-VMName</span></span>
<span data-ttu-id="97a83-126">Gibt den Namen eines virtuellen Computers an.</span><span class="sxs-lookup"><span data-stu-id="97a83-126">Specifies the name of a virtual machine.</span></span>

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

### <span data-ttu-id="97a83-127">-Windows</span><span class="sxs-lookup"><span data-stu-id="97a83-127">-Windows</span></span>
<span data-ttu-id="97a83-128">Gibt an, dass dieses Cmdlet für einen virtuellen Windows-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="97a83-128">Indicates that this cmdlet is for a Windows virtual machine.</span></span>

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

### <span data-ttu-id="97a83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a83-129">CommonParameters</span></span>
<span data-ttu-id="97a83-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a83-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="97a83-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a83-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="97a83-132">INPUTS</span></span>

### <span data-ttu-id="97a83-133">System.String</span><span class="sxs-lookup"><span data-stu-id="97a83-133">System.String</span></span>

### <span data-ttu-id="97a83-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97a83-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97a83-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="97a83-135">OUTPUTS</span></span>

### <span data-ttu-id="97a83-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="97a83-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="97a83-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="97a83-137">NOTES</span></span>

## <span data-ttu-id="97a83-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="97a83-138">RELATED LINKS</span></span>

[<span data-ttu-id="97a83-139">Set-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="97a83-139">Set-AzVMChefExtension</span></span>](./Set-AzVMChefExtension.md)

[<span data-ttu-id="97a83-140">Remove-AzVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="97a83-140">Remove-AzVMChefExtension</span></span>](./Remove-AzVMChefExtension.md)


