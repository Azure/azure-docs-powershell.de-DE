---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 49D17667-35C3-4A79-A0C8-C197DAA5CD90
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaddomainextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMADDomainExtension.md
ms.openlocfilehash: ca6b3d4863629aa94585db9850042fff4165dd10
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005272"
---
# <span data-ttu-id="a262f-101">Get-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a262f-101">Get-AzVMADDomainExtension</span></span>

## <span data-ttu-id="a262f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a262f-102">SYNOPSIS</span></span>
<span data-ttu-id="a262f-103">Ruft Informationen zu einer AD-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a262f-103">Gets information about an AD domain extension.</span></span>

## <span data-ttu-id="a262f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a262f-104">SYNTAX</span></span>

```
Get-AzVMADDomainExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a262f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a262f-105">DESCRIPTION</span></span>
<span data-ttu-id="a262f-106">Das Cmdlet " **Get-AzVMADDomainExtension** " Ruft Informationen zur angegebenen Azure Active Directory (AD)-Domänenerweiterung ab.</span><span class="sxs-lookup"><span data-stu-id="a262f-106">The **Get-AzVMADDomainExtension** cmdlet gets information about the specified Azure Active Directory (AD) domain extension.</span></span>

## <span data-ttu-id="a262f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a262f-107">EXAMPLES</span></span>

## <span data-ttu-id="a262f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a262f-108">PARAMETERS</span></span>

### <span data-ttu-id="a262f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a262f-109">-DefaultProfile</span></span>
<span data-ttu-id="a262f-110">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a262f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a262f-111">-Name</span><span class="sxs-lookup"><span data-stu-id="a262f-111">-Name</span></span>
<span data-ttu-id="a262f-112">Gibt den Namen der Domänenerweiterung an.</span><span class="sxs-lookup"><span data-stu-id="a262f-112">Specifies the name of the domain extension.</span></span>

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

### <span data-ttu-id="a262f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a262f-113">-ResourceGroupName</span></span>
<span data-ttu-id="a262f-114">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a262f-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="a262f-115">-Status</span><span class="sxs-lookup"><span data-stu-id="a262f-115">-Status</span></span>
<span data-ttu-id="a262f-116">Gibt an, dass dieses Cmdlet die Instanzen Ansicht der Domänenerweiterung abruft.</span><span class="sxs-lookup"><span data-stu-id="a262f-116">Indicates that this cmdlet gets the instance view of the domain extension.</span></span>

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

### <span data-ttu-id="a262f-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="a262f-117">-VMName</span></span>
<span data-ttu-id="a262f-118">Gibt den Namen der virtuellen Maschine an.</span><span class="sxs-lookup"><span data-stu-id="a262f-118">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="a262f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a262f-119">CommonParameters</span></span>
<span data-ttu-id="a262f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a262f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a262f-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a262f-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a262f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a262f-122">INPUTS</span></span>

### <span data-ttu-id="a262f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a262f-123">System.String</span></span>

### <span data-ttu-id="a262f-124">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a262f-124">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a262f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a262f-125">OUTPUTS</span></span>

### <span data-ttu-id="a262f-126">Microsoft. Azure. Commands. Compute. Models. VirtualMachineADDomainExtensionContext</span><span class="sxs-lookup"><span data-stu-id="a262f-126">Microsoft.Azure.Commands.Compute.Models.VirtualMachineADDomainExtensionContext</span></span>

## <span data-ttu-id="a262f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="a262f-127">NOTES</span></span>

## <span data-ttu-id="a262f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a262f-128">RELATED LINKS</span></span>

[<span data-ttu-id="a262f-129">Satz-AzVMADDomainExtension</span><span class="sxs-lookup"><span data-stu-id="a262f-129">Set-AzVMADDomainExtension</span></span>](./Set-AzVMADDomainExtension.md)


