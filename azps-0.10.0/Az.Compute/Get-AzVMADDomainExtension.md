---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: 809246520c4e6b07a1aca406ef3ec17eb9df31f1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844632"
---
# <span data-ttu-id="0a16b-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0a16b-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="0a16b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a16b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a16b-103">Ruft Informationen zu einer AD-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="0a16b-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="0a16b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a16b-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a16b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a16b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a16b-106">Das Cmdlet " **Get-AzVMADDomainExtension** " Ruft Informationen zur angegebenen Azure Active Directory (AD)-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="0a16b-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="0a16b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a16b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a16b-108">1:</span><span class="sxs-lookup"><span data-stu-id="0a16b-108">1:</span></span>
```

```

## <span data-ttu-id="0a16b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a16b-109">PARAMETERS</span></span>

### <span data-ttu-id="0a16b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a16b-110">-DefaultProfile</span></span>
<span data-ttu-id="0a16b-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0a16b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a16b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="0a16b-112">-Name</span></span>
<span data-ttu-id="0a16b-113">Gibt den Namen der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="0a16b-113">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="0a16b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a16b-114">-ResourceGroupName</span></span>
<span data-ttu-id="0a16b-115">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0a16b-115">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0a16b-116">-Status</span><span class="sxs-lookup"><span data-stu-id="0a16b-116">-Status</span></span>
<span data-ttu-id="0a16b-117">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der Domänenerweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="0a16b-117">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="0a16b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="0a16b-118">-VMName</span></span>
<span data-ttu-id="0a16b-119">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="0a16b-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="0a16b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a16b-120">CommonParameters</span></span>
<span data-ttu-id="0a16b-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a16b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a16b-122">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a16b-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a16b-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a16b-123">INPUTS</span></span>

### <span data-ttu-id="0a16b-124">Keine</span><span class="sxs-lookup"><span data-stu-id="0a16b-124">None</span></span>
<span data-ttu-id="0a16b-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0a16b-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a16b-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a16b-126">OUTPUTS</span></span>

### <span data-ttu-id="0a16b-127">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="0a16b-127">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="0a16b-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a16b-128">NOTES</span></span>

## <span data-ttu-id="0a16b-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a16b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0a16b-130">Satz-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="0a16b-130">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


