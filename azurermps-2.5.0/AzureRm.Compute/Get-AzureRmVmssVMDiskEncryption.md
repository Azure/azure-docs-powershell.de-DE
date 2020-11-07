---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmssvmdiskencryption
schema: 2.0.0
ms.openlocfilehash: 41c18a3f9b1536e837ab8e127bfe00b62c74b5e1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850460"
---
# <span data-ttu-id="36ca4-101">Get-AzureRmVmssVMDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="36ca4-101">Get-AzureRmVmssVMDiskEncryption</span></span>

## <span data-ttu-id="36ca4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36ca4-102">SYNOPSIS</span></span>
<span data-ttu-id="36ca4-103">Zeigt den Datenträger Verschlüsselungsstatus von VMS in einem VM-Skalierungs Satz.</span><span class="sxs-lookup"><span data-stu-id="36ca4-103">Shows the disk encryption status of VMs in a VM scale set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36ca4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36ca4-104">SYNTAX</span></span>

```
Get-AzureRmVmssVMDiskEncryption [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [[-InstanceId] <String>] [-ExtensionName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36ca4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36ca4-105">DESCRIPTION</span></span>
<span data-ttu-id="36ca4-106">Zeigt den Datenträger Verschlüsselungsstatus des VM-Skalierungs Satzes an.</span><span class="sxs-lookup"><span data-stu-id="36ca4-106">Shows the disk encryption status of VM scale set.</span></span>

## <span data-ttu-id="36ca4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36ca4-107">EXAMPLES</span></span>

### <span data-ttu-id="36ca4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="36ca4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVmssVMDiskEncryption -ResourceGroupName "Group001" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="36ca4-109">Zeigt den Datenträger Verschlüsselungsstatus der VM-Instanz 1 im VM-Skalierungs Satz mit dem Namen VMSS001, der zur Ressourcengruppe mit dem Namen Group001 gehört.</span><span class="sxs-lookup"><span data-stu-id="36ca4-109">Shows the disk encryption status of VM instance 1 in the VM scale set named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="36ca4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="36ca4-110">PARAMETERS</span></span>

### <span data-ttu-id="36ca4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ca4-111">-DefaultProfile</span></span>
<span data-ttu-id="36ca4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36ca4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36ca4-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="36ca4-113">-ExtensionName</span></span>
<span data-ttu-id="36ca4-114">Der Name der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="36ca4-114">The extension name.</span></span>
<span data-ttu-id="36ca4-115">Wenn dieser Parameter nicht angegeben ist, werden die Standardwerte AzureDiskEncryption für Windows VMS und AzureDiskEncryptionForLinux für Linux VMs verwendet.</span><span class="sxs-lookup"><span data-stu-id="36ca4-115">If this parameter is not specified, default values used are AzureDiskEncryption for windows VMs and AzureDiskEncryptionForLinux for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca4-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="36ca4-116">-InstanceId</span></span>
<span data-ttu-id="36ca4-117">Gibt die Instanz-ID an.</span><span class="sxs-lookup"><span data-stu-id="36ca4-117">Specifies the instance ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ca4-118">-ResourceGroupName</span></span>
<span data-ttu-id="36ca4-119">Ressourcengruppenname des Skalierungs Satzes für virtuelle Maschinen</span><span class="sxs-lookup"><span data-stu-id="36ca4-119">Resource group name of the virtual machine scale set.</span></span>

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

### <span data-ttu-id="36ca4-120">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="36ca4-120">-VMScaleSetName</span></span>
<span data-ttu-id="36ca4-121">Der Skalierungs Satz Name des virtuellen Computers.</span><span class="sxs-lookup"><span data-stu-id="36ca4-121">The virtual machine scale set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36ca4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ca4-122">CommonParameters</span></span>
<span data-ttu-id="36ca4-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36ca4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ca4-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36ca4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ca4-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36ca4-125">INPUTS</span></span>

### <span data-ttu-id="36ca4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="36ca4-126">System.String</span></span>

## <span data-ttu-id="36ca4-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36ca4-127">OUTPUTS</span></span>

### <span data-ttu-id="36ca4-128">Microsoft. Azure. Commands. Compute. Models. PSVmssVMDiskEncryptionStatusContext</span><span class="sxs-lookup"><span data-stu-id="36ca4-128">Microsoft.Azure.Commands.Compute.Models.PSVmssVMDiskEncryptionStatusContext</span></span>

## <span data-ttu-id="36ca4-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="36ca4-129">NOTES</span></span>

## <span data-ttu-id="36ca4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36ca4-130">RELATED LINKS</span></span>

