---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssVMDiskEncryption.md
ms.openlocfilehash: 551e5928ca4628b9964132ee117cbf65fdbaedba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476213"
---
# <span data-ttu-id="e31b6-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e31b6-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="e31b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e31b6-102">SYNOPSIS</span></span>
<span data-ttu-id="e31b6-103">Zeigt den Datenträger Verschlüsselungsstatus von VMS in einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="e31b6-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e31b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31b6-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e31b6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e31b6-105">DESCRIPTION</span></span>
<span data-ttu-id="e31b6-106">Zeigt den Datenträger Verschlüsselungsstatus des VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="e31b6-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="e31b6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e31b6-107">EXAMPLES</span></span>

### <span data-ttu-id="e31b6-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e31b6-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="e31b6-109">Zeigt den Datenträger Verschlüsselungsstatus der VM-Instanz 1 im VM-Skalierungs Satz mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="e31b6-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="e31b6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e31b6-110">PARAMETERS</span></span>

### <span data-ttu-id="e31b6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e31b6-111">-DefaultProfile</span></span>
<span data-ttu-id="e31b6-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e31b6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e31b6-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="e31b6-113">-ExtensionName</span></span>
<span data-ttu-id="e31b6-114">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="e31b6-114">The extension name.</span></span>
<span data-ttu-id="e31b6-115">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="e31b6-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31b6-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e31b6-116">-InstanceId</span></span>
<span data-ttu-id="e31b6-117">Gibt die Instanz-ID an.</span><span class="sxs-lookup"><span data-stu-id="e31b6-117">Specifies the instance ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31b6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e31b6-118">-ResourceGroupName</span></span>
<span data-ttu-id="e31b6-119">Ressourcengruppenname des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="e31b6-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="e31b6-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e31b6-120">-VMScaleSetName</span></span>
<span data-ttu-id="e31b6-121">Der Skalierungs Satz Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="e31b6-121">The virtual machine scale set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e31b6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e31b6-122">CommonParameters</span></span>
<span data-ttu-id="e31b6-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e31b6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e31b6-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e31b6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e31b6-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e31b6-125">INPUTS</span></span>

### <span data-ttu-id="e31b6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e31b6-126">System.String</span></span>

## <span data-ttu-id="e31b6-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e31b6-127">OUTPUTS</span></span>

### <span data-ttu-id="e31b6-128">Microsoft. Azure. Commands. Compute. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="e31b6-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="e31b6-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="e31b6-129">NOTES</span></span>

## <span data-ttu-id="e31b6-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e31b6-130">RELATED LINKS</span></span>
