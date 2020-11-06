---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: d55d84560ca75a508a05276d8d33eb78d1d50ab5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497726"
---
# <span data-ttu-id="30291-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="30291-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="30291-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="30291-102">SYNOPSIS</span></span>
<span data-ttu-id="30291-103">Ruft Informationen zu einer AD-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="30291-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30291-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="30291-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="30291-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30291-105">DESCRIPTION</span></span>
<span data-ttu-id="30291-106">Das Cmdlet " **Get-AzureRmVMADDomainExtension** " Ruft Informationen zur angegebenen Azure Active Directory (AD)-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="30291-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="30291-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="30291-107">EXAMPLES</span></span>

## <span data-ttu-id="30291-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="30291-108">PARAMETERS</span></span>

### <span data-ttu-id="30291-109">-Name</span><span class="sxs-lookup"><span data-stu-id="30291-109">-Name</span></span>
<span data-ttu-id="30291-110">Gibt den Namen der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="30291-110">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="30291-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30291-111">-ResourceGroupName</span></span>
<span data-ttu-id="30291-112">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="30291-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="30291-113">-Status</span><span class="sxs-lookup"><span data-stu-id="30291-113">-Status</span></span>
<span data-ttu-id="30291-114">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der Domänenerweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="30291-114">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="30291-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="30291-115">-VMName</span></span>
<span data-ttu-id="30291-116">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="30291-116">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="30291-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30291-117">CommonParameters</span></span>
<span data-ttu-id="30291-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30291-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30291-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30291-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30291-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="30291-120">INPUTS</span></span>

### <span data-ttu-id="30291-121">Keine</span><span class="sxs-lookup"><span data-stu-id="30291-121">None</span></span>
<span data-ttu-id="30291-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="30291-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30291-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="30291-123">OUTPUTS</span></span>

## <span data-ttu-id="30291-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="30291-124">NOTES</span></span>

## <span data-ttu-id="30291-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="30291-125">RELATED LINKS</span></span>

[<span data-ttu-id="30291-126">Satz-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="30291-126">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


