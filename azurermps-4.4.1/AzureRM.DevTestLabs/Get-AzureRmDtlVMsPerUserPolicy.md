---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 5029179A-99A5-4350-A8E5-D15ABA59CC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlVMsPerUserPolicy.md
ms.openlocfilehash: 2be26f222be7ec444706fb15fb862a43dc8b8116
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501889"
---
# <span data-ttu-id="60ce7-101">Get-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="60ce7-101">Get-AzureRmDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="60ce7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60ce7-102">SYNOPSIS</span></span>
<span data-ttu-id="60ce7-103">Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit in DevTest Labs ab.</span><span class="sxs-lookup"><span data-stu-id="60ce7-103">Gets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60ce7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60ce7-104">SYNTAX</span></span>

```
Get-AzureRmDtlVMsPerUserPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60ce7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60ce7-105">DESCRIPTION</span></span>
<span data-ttu-id="60ce7-106">Das Cmdlet " **Get-AzureRmDtlVMsPerUserPolicy** " Ruft die virtuellen Computer pro Benutzerrichtlinie einer Übungseinheit ab, mit der Sie die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer festlegen können.</span><span class="sxs-lookup"><span data-stu-id="60ce7-106">The **Get-AzureRmDtlVMsPerUserPolicy** cmdlet gets the virtual machines per user policy of a lab, which allows you to set the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="60ce7-107">Das Cmdlet gibt den aktivierten oder deaktivierten Status der Richtlinie und die maximale Anzahl der pro Benutzer zulässigen virtuellen Computer zurück, die Sie in der Richtlinie festgesetzt haben.</span><span class="sxs-lookup"><span data-stu-id="60ce7-107">The cmdlet returns the enabled or disabled status of the policy and the maximum number of virtual machines allowed per user that you have set in the policy.</span></span>

## <span data-ttu-id="60ce7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60ce7-108">EXAMPLES</span></span>

## <span data-ttu-id="60ce7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="60ce7-109">PARAMETERS</span></span>

### <span data-ttu-id="60ce7-110">-LabName</span><span class="sxs-lookup"><span data-stu-id="60ce7-110">-LabName</span></span>
<span data-ttu-id="60ce7-111">Gibt den Namen der Übungseinheit an, für die dieses Cmdlet den virtuellen Computer pro Benutzerrichtlinie abruft.</span><span class="sxs-lookup"><span data-stu-id="60ce7-111">Specifies the name of the lab for which this cmdlet gets the virtual machine per user policy.</span></span>

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

### <span data-ttu-id="60ce7-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ce7-112">-ResourceGroupName</span></span>
<span data-ttu-id="60ce7-113">Gibt den Namen der Ressourcengruppe an, zu der die Übungseinheit gehört.</span><span class="sxs-lookup"><span data-stu-id="60ce7-113">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="60ce7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ce7-114">-DefaultProfile</span></span>
<span data-ttu-id="60ce7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60ce7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60ce7-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ce7-116">CommonParameters</span></span>
<span data-ttu-id="60ce7-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ce7-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ce7-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60ce7-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ce7-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60ce7-119">INPUTS</span></span>

## <span data-ttu-id="60ce7-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60ce7-120">OUTPUTS</span></span>

### <span data-ttu-id="60ce7-121">Microsoft. Azure. Commands. DevTestLabs. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="60ce7-121">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="60ce7-122">Dieses Cmdlet gibt die Richtlinie zurück, die die maximale Anzahl virtueller Computer angibt, die von einem Benutzer in der Übungseinheit erstellt werden können.</span><span class="sxs-lookup"><span data-stu-id="60ce7-122">This cmdlet returns the policy that specifies the maximum number of virtual machines that can be created by a user in the lab.</span></span>

## <span data-ttu-id="60ce7-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="60ce7-123">NOTES</span></span>

## <span data-ttu-id="60ce7-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60ce7-124">RELATED LINKS</span></span>

[<span data-ttu-id="60ce7-125">Satz-AzureRmDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="60ce7-125">Set-AzureRmDtlVMsPerUserPolicy</span></span>](./Set-AzureRmDtlVMsPerUserPolicy.md)


