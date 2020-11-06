---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: A3F653C7-6F9D-4B2B-81F8-0A012D80ECC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerLabPolicy.md
ms.openlocfilehash: 3f38c8ace41a1f125a37053f136cd61c597787ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482485"
---
# <span data-ttu-id="7b2c9-101">Get-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="7b2c9-101">Get-AzureRmDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="7b2c9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b2c9-103">Ruft die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-103">Gets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b2c9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b2c9-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerLabPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b2c9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b2c9-105">DESCRIPTION</span></span>
<span data-ttu-id="7b2c9-106">Das Cmdlet " **Get-AzureRmDtlVMsPerLabPolicy** " Ruft die virtuellen Computer pro Lab-Richtlinie einer Übungseinheit ab, wodurch Sie die Gesamtzahl der in einer Übungseinheit zulässigen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-106">The **Get-AzureRmDtlVMsPerLabPolicy** cmdlet gets the virtual machines per lab policy of a lab, which allows you set the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="7b2c9-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die Gesamtanzahl der in der Übungseinheit zulässigen virtuellen Computer zurück, die Sie in der Richtlinie festgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-107">The cmdlet returns the enabled or disabled status of the policy, and the total number of virtual machines allowed in the lab that you have set in the policy.</span></span>

## <span data-ttu-id="7b2c9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b2c9-108">EXAMPLES</span></span>

## <span data-ttu-id="7b2c9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b2c9-109">PARAMETERS</span></span>

### <span data-ttu-id="7b2c9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b2c9-110">-DefaultProfile</span></span>
<span data-ttu-id="7b2c9-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7b2c9-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b2c9-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="7b2c9-112">-LabName</span></span>
<span data-ttu-id="7b2c9-113">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet die virtuellen Computer abruft.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-113">Specifies the name of the lab for which this cmdlet gets the virtual machines.</span></span>

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

### <span data-ttu-id="7b2c9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b2c9-114">-ResourceGroupName</span></span>
<span data-ttu-id="7b2c9-115">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="7b2c9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b2c9-116">CommonParameters</span></span>
<span data-ttu-id="7b2c9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b2c9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b2c9-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b2c9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b2c9-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b2c9-119">INPUTS</span></span>

### <span data-ttu-id="7b2c9-120">System. String</span><span class="sxs-lookup"><span data-stu-id="7b2c9-120">System.String</span></span>

## <span data-ttu-id="7b2c9-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b2c9-121">OUTPUTS</span></span>

### <span data-ttu-id="7b2c9-122">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="7b2c9-122">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="7b2c9-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b2c9-123">NOTES</span></span>

## <span data-ttu-id="7b2c9-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b2c9-124">RELATED LINKS</span></span>

[<span data-ttu-id="7b2c9-125">Satz-AzureRmDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="7b2c9-125">Set-AzureRmDtlVMsPerLabPolicy</span></span>](./Set-AzureRmDtlVMsPerLabPolicy.md)


