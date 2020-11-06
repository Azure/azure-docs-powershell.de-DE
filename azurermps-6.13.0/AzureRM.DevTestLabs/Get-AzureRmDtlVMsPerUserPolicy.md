---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 4d8bf2922d58190e41e71e17c96ab55b5ee9433f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482481"
---
# <span data-ttu-id="7ceac-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="7ceac-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="7ceac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ceac-102">SYNOPSIS</span></span>
<span data-ttu-id="7ceac-103">Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="7ceac-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ceac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ceac-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ceac-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ceac-105">DESCRIPTION</span></span>
<span data-ttu-id="7ceac-106">Das Cmdlet " **Get-AzureRmDtlVMsPerUserPolicy** " Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit ab, mit der Sie die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="7ceac-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="7ceac-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer zurück, die Sie in der Richtlinie festgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="7ceac-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="7ceac-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ceac-108">EXAMPLES</span></span>

## <span data-ttu-id="7ceac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ceac-109">PARAMETERS</span></span>

### <span data-ttu-id="7ceac-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ceac-110">-DefaultProfile</span></span>
<span data-ttu-id="7ceac-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ceac-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ceac-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="7ceac-112">-LabName</span></span>
<span data-ttu-id="7ceac-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet den virtuellen Computer pro Benutzerrichtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="7ceac-113">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="7ceac-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ceac-114">-ResourceGroupName</span></span>
<span data-ttu-id="7ceac-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="7ceac-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="7ceac-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ceac-116">CommonParameters</span></span>
<span data-ttu-id="7ceac-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ceac-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ceac-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ceac-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ceac-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ceac-119">INPUTS</span></span>

### <span data-ttu-id="7ceac-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7ceac-120">System.String</span></span>

## <span data-ttu-id="7ceac-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ceac-121">OUTPUTS</span></span>

### <span data-ttu-id="7ceac-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="7ceac-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="7ceac-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ceac-123">NOTES</span></span>

## <span data-ttu-id="7ceac-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ceac-124">RELATED LINKS</span></span>

[<span data-ttu-id="7ceac-125">Satz-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="7ceac-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


