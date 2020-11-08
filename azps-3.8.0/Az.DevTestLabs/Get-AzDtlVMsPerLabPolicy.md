---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 29d887639dd88f85a24144a4482c40c2b7626c7e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997061"
---
# <span data-ttu-id="1f6b8-101">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1f6b8-101">Get-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="1f6b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f6b8-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6b8-103">Ruft die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="1f6b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f6b8-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f6b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f6b8-105">DESCRIPTION</span></span>
<span data-ttu-id="1f6b8-106">Das Cmdlet " **Get-AzDtlVMsPerLabPolicy** " Ruft die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit ab, wodurch Sie die Gesamtzahl der in einer Übungseinheit zulässigen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-106">The **Get-AzDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="1f6b8-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die Gesamtanzahl der in der Übungseinheit zulässigen virtuellen Computer zurück, die Sie in der Richtlinie festgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="1f6b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f6b8-108">EXAMPLES</span></span>

## <span data-ttu-id="1f6b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f6b8-109">PARAMETERS</span></span>

### <span data-ttu-id="1f6b8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6b8-110">-DefaultProfile</span></span>
<span data-ttu-id="1f6b8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1f6b8-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1f6b8-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="1f6b8-112">-LabName</span></span>
<span data-ttu-id="1f6b8-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die virtuellen Computer abruft.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="1f6b8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6b8-114">-ResourceGroupName</span></span>
<span data-ttu-id="1f6b8-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="1f6b8-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6b8-116">CommonParameters</span></span>
<span data-ttu-id="1f6b8-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6b8-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6b8-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6b8-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6b8-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f6b8-119">INPUTS</span></span>

### <span data-ttu-id="1f6b8-120">System. String</span><span class="sxs-lookup"><span data-stu-id="1f6b8-120">System.String</span></span>

## <span data-ttu-id="1f6b8-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f6b8-121">OUTPUTS</span></span>

### <span data-ttu-id="1f6b8-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1f6b8-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="1f6b8-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f6b8-123">NOTES</span></span>

## <span data-ttu-id="1f6b8-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f6b8-124">RELATED LINKS</span></span>

[<span data-ttu-id="1f6b8-125">Satz-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="1f6b8-125">Set-AzDtlVMsPerLabPolicy</span></span>](./Set-AzDtlVMsPerLabPolicy.md)


