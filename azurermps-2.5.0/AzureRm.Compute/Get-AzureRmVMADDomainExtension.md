---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
ms.openlocfilehash: 01a5a69053cfd05186abae45d5b53fff0b022b98
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848900"
---
# <span data-ttu-id="fc7d4-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fc7d4-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="fc7d4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="fc7d4-103">Ruft Informationen zu einer AD-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc7d4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc7d4-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc7d4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc7d4-105">DESCRIPTION</span></span>
<span data-ttu-id="fc7d4-106">Das Cmdlet " **Get-AzureRmVMADDomainExtension** " Ruft Informationen zur angegebenen Azure Active Directory (AD)-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="fc7d4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc7d4-107">EXAMPLES</span></span>

### <span data-ttu-id="fc7d4-108">1:</span><span class="sxs-lookup"><span data-stu-id="fc7d4-108">1:</span></span>
```

```

## <span data-ttu-id="fc7d4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc7d4-109">PARAMETERS</span></span>

### <span data-ttu-id="fc7d4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc7d4-110">-DefaultProfile</span></span>
<span data-ttu-id="fc7d4-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc7d4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="fc7d4-112">-Name</span></span>
<span data-ttu-id="fc7d4-113">Gibt den Namen der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-113">Specifies the name of the domain extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d4-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc7d4-114">-ResourceGroupName</span></span>
<span data-ttu-id="fc7d4-115">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="fc7d4-116">-Status</span><span class="sxs-lookup"><span data-stu-id="fc7d4-116">-Status</span></span>
<span data-ttu-id="fc7d4-117">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der Domänenerweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc7d4-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="fc7d4-118">-VMName</span></span>
<span data-ttu-id="fc7d4-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fc7d4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc7d4-120">CommonParameters</span></span>
<span data-ttu-id="fc7d4-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc7d4-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc7d4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc7d4-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc7d4-123">INPUTS</span></span>

### <span data-ttu-id="fc7d4-124">Keine</span><span class="sxs-lookup"><span data-stu-id="fc7d4-124">None</span></span>
<span data-ttu-id="fc7d4-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="fc7d4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fc7d4-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc7d4-126">OUTPUTS</span></span>

### <span data-ttu-id="fc7d4-127">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="fc7d4-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="fc7d4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc7d4-128">NOTES</span></span>

## <span data-ttu-id="fc7d4-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc7d4-129">RELATED LINKS</span></span>

[<span data-ttu-id="fc7d4-130">Satz-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="fc7d4-130">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


