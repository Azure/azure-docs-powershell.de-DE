---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c906d7b0b10197e934ace7f9c913ee36e02be7ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502210"
---
# <span data-ttu-id="b9722-101">Get-AzureRmVmssSku</span><span class="sxs-lookup"><span data-stu-id="b9722-101">Get-AzureRmVmssSku</span></span>

## <span data-ttu-id="b9722-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b9722-102">SYNOPSIS</span></span>
<span data-ttu-id="b9722-103">Ruft die verfügbaren SKUs für das VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="b9722-103">Gets the available SKUs for the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b9722-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9722-104">SYNTAX</span></span>

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9722-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9722-105">DESCRIPTION</span></span>
<span data-ttu-id="b9722-106">Das Cmdlet " **Get-AzureRmVmssSku** " Ruft die verfügbaren SKUs für den virtuellen Computer-Skalierungs Satz (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="b9722-106">The **Get-AzureRmVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="b9722-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9722-107">EXAMPLES</span></span>

### <span data-ttu-id="b9722-108">Beispiel 1: Abrufen aller verfügbaren SKUs vom VMSS</span><span class="sxs-lookup"><span data-stu-id="b9722-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="b9722-109">Dieser Befehl ruft alle verfügbaren SKUs aus dem VMSS mit dem Namen ContosoVMSS ab, das zur Ressourcengruppe namens contosogroup gehört.</span><span class="sxs-lookup"><span data-stu-id="b9722-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="b9722-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9722-110">PARAMETERS</span></span>

### <span data-ttu-id="b9722-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9722-111">-DefaultProfile</span></span>
<span data-ttu-id="b9722-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b9722-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9722-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9722-113">-ResourceGroupName</span></span>
<span data-ttu-id="b9722-114">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="b9722-114">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9722-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="b9722-115">-VMScaleSetName</span></span>
<span data-ttu-id="b9722-116">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="b9722-116">Species the name of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9722-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9722-117">CommonParameters</span></span>
<span data-ttu-id="b9722-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9722-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9722-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9722-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9722-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b9722-120">INPUTS</span></span>

### <span data-ttu-id="b9722-121">System. String</span><span class="sxs-lookup"><span data-stu-id="b9722-121">System.String</span></span>

## <span data-ttu-id="b9722-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b9722-122">OUTPUTS</span></span>

### <span data-ttu-id="b9722-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="b9722-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="b9722-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="b9722-124">NOTES</span></span>

## <span data-ttu-id="b9722-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b9722-125">RELATED LINKS</span></span>

[<span data-ttu-id="b9722-126">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="b9722-126">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


