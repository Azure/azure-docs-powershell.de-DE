---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMADDomainExtension.md
ms.openlocfilehash: 398cc4b8f23ca5296aec741eb720833f589b0e2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480477"
---
# <span data-ttu-id="68b3b-101">Get-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="68b3b-101">Get-AzureRmVMADDomainExtension</span></span>

## <span data-ttu-id="68b3b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="68b3b-103">Ruft Informationen zu einer AD-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="68b3b-103">Gets information about an AD domain extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68b3b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68b3b-104">SYNTAX</span></span>

```
Get-AzureRmVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68b3b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68b3b-105">DESCRIPTION</span></span>
<span data-ttu-id="68b3b-106">Das Cmdlet " **Get-AzureRmVMADDomainExtension** " Ruft Informationen zur angegebenen Azure Active Directory (AD)-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="68b3b-106">The **Get-AzureRmVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="68b3b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68b3b-107">EXAMPLES</span></span>

## <span data-ttu-id="68b3b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="68b3b-108">PARAMETERS</span></span>

### <span data-ttu-id="68b3b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68b3b-109">-DefaultProfile</span></span>
<span data-ttu-id="68b3b-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="68b3b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="68b3b-111">-Name</span><span class="sxs-lookup"><span data-stu-id="68b3b-111">-Name</span></span>
<span data-ttu-id="68b3b-112">Gibt den Namen der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="68b3b-112">Specifies the name of the domain extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68b3b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68b3b-113">-ResourceGroupName</span></span>
<span data-ttu-id="68b3b-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="68b3b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="68b3b-115">-Status</span><span class="sxs-lookup"><span data-stu-id="68b3b-115">-Status</span></span>
<span data-ttu-id="68b3b-116">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der Domänenerweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="68b3b-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="68b3b-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="68b3b-117">-VMName</span></span>
<span data-ttu-id="68b3b-118">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="68b3b-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="68b3b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68b3b-119">CommonParameters</span></span>
<span data-ttu-id="68b3b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68b3b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68b3b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68b3b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68b3b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68b3b-122">INPUTS</span></span>

### <span data-ttu-id="68b3b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="68b3b-123">System.String</span></span>

### <span data-ttu-id="68b3b-124">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="68b3b-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="68b3b-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68b3b-125">OUTPUTS</span></span>

### <span data-ttu-id="68b3b-126">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="68b3b-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="68b3b-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="68b3b-127">NOTES</span></span>

## <span data-ttu-id="68b3b-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68b3b-128">RELATED LINKS</span></span>

[<span data-ttu-id="68b3b-129">Satz-AzureRmVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="68b3b-129">Set-AzureRmVMADDomainExtension</span></span>](./Set-AzureRmVMADDomainExtension.md)


