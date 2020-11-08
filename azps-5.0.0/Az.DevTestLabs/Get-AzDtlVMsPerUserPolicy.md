---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/get-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Get-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: f2d8604de126dcdfa830bdd6650cf66a6db391b5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175753"
---
# <span data-ttu-id="a2b91-101">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="a2b91-101">Get-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="a2b91-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2b91-102">SYNOPSIS</span></span>
<span data-ttu-id="a2b91-103">Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="a2b91-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a2b91-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2b91-104">SYNTAX</span></span>

```
Get-AzDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2b91-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2b91-105">DESCRIPTION</span></span>
<span data-ttu-id="a2b91-106">Das Cmdlet " **Get-AzDtlVMsPerUserPolicy** " Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit ab, mit der Sie die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="a2b91-106">The **Get-AzDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="a2b91-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer zurück, die Sie in der Richtlinie festgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="a2b91-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="a2b91-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2b91-108">EXAMPLES</span></span>

## <span data-ttu-id="a2b91-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2b91-109">PARAMETERS</span></span>

### <span data-ttu-id="a2b91-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2b91-110">-DefaultProfile</span></span>
<span data-ttu-id="a2b91-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a2b91-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2b91-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="a2b91-112">-LabName</span></span>
<span data-ttu-id="a2b91-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet den virtuellen Computer pro Benutzerrichtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="a2b91-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="a2b91-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2b91-114">-ResourceGroupName</span></span>
<span data-ttu-id="a2b91-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="a2b91-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a2b91-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2b91-116">CommonParameters</span></span>
<span data-ttu-id="a2b91-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2b91-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2b91-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2b91-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2b91-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2b91-119">INPUTS</span></span>

### <span data-ttu-id="a2b91-120">System. String</span><span class="sxs-lookup"><span data-stu-id="a2b91-120">System.String</span></span>

## <span data-ttu-id="a2b91-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2b91-121">OUTPUTS</span></span>

### <span data-ttu-id="a2b91-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a2b91-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a2b91-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2b91-123">NOTES</span></span>

## <span data-ttu-id="a2b91-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2b91-124">RELATED LINKS</span></span>

[<span data-ttu-id="a2b91-125">Satz-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="a2b91-125">Set-AzDtlVMsPerUserPolicy</span></span>](./Set-AzDtlVMsPerUserPolicy.md)


