---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsssku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssSku.md
ms.openlocfilehash: 4b17cbb748a9841e0c22f4b8d8742562876fb9db
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995186"
---
# <span data-ttu-id="8c7f1-101">Get-AzVmssSku</span><span class="sxs-lookup"><span data-stu-id="8c7f1-101">Get-AzVmssSku</span></span>

## <span data-ttu-id="8c7f1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c7f1-102">SYNOPSIS</span></span>
<span data-ttu-id="8c7f1-103">Ruft die verfügbaren SKUs für das VMSS ab.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-103">Gets the available SKUs for the VMSS.</span></span>

## <span data-ttu-id="8c7f1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c7f1-104">SYNTAX</span></span>

```
Get-AzVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8c7f1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c7f1-105">DESCRIPTION</span></span>
<span data-ttu-id="8c7f1-106">Das Cmdlet " **Get-AzVmssSku** " Ruft die verfügbaren SKUs für den virtuellen Computer-Skalierungs Satz (VMSS) ab.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-106">The **Get-AzVmssSku** cmdlet gets the available SKUs for the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="8c7f1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c7f1-107">EXAMPLES</span></span>

### <span data-ttu-id="8c7f1-108">Beispiel 1: Abrufen aller verfügbaren SKUs vom VMSS</span><span class="sxs-lookup"><span data-stu-id="8c7f1-108">Example 1: Get all available SKUs from the VMSS</span></span>
```
PS C:\> Get-AzVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="8c7f1-109">Dieser Befehl ruft alle verfügbaren SKUs aus dem VMSS mit dem Namen ContosoVMSS ab, das zur Ressourcengruppe namens contosogroup gehört.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-109">This command gets all the available SKUs from the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="8c7f1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c7f1-110">PARAMETERS</span></span>

### <span data-ttu-id="8c7f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c7f1-111">-DefaultProfile</span></span>
<span data-ttu-id="8c7f1-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c7f1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c7f1-113">-ResourceGroupName</span></span>
<span data-ttu-id="8c7f1-114">Gibt den Namen der Ressourcengruppe des VMSS an.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-114">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="8c7f1-115">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="8c7f1-115">-VMScaleSetName</span></span>
<span data-ttu-id="8c7f1-116">Art der Name des VMSS.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-116">Species the name of the VMSS.</span></span>

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

### <span data-ttu-id="8c7f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c7f1-117">CommonParameters</span></span>
<span data-ttu-id="8c7f1-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c7f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c7f1-119">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c7f1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c7f1-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c7f1-120">INPUTS</span></span>

### <span data-ttu-id="8c7f1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8c7f1-121">System.String</span></span>

## <span data-ttu-id="8c7f1-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c7f1-122">OUTPUTS</span></span>

### <span data-ttu-id="8c7f1-123">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSetSku</span><span class="sxs-lookup"><span data-stu-id="8c7f1-123">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetSku</span></span>

## <span data-ttu-id="8c7f1-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c7f1-124">NOTES</span></span>

## <span data-ttu-id="8c7f1-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c7f1-125">RELATED LINKS</span></span>

[<span data-ttu-id="8c7f1-126">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="8c7f1-126">Get-AzVmss</span></span>](./Get-AzVmss.md)


