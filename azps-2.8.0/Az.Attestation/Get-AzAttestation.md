---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/get-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Get-AzAttestation.md
ms.openlocfilehash: cd6181ffb2bba8d71d8a0bf7cbe96d2f8038efc5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658090"
---
# <span data-ttu-id="08152-101">Get-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="08152-101">Get-AzAttestation</span></span>

## <span data-ttu-id="08152-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08152-102">SYNOPSIS</span></span>
<span data-ttu-id="08152-103">Ruft eine Bescheinigung ab.</span><span class="sxs-lookup"><span data-stu-id="08152-103">Gets an attestation.</span></span>

## <span data-ttu-id="08152-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08152-104">SYNTAX</span></span>

### <span data-ttu-id="08152-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="08152-105">NameParameterSet (Default)</span></span>
```
Get-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08152-106">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="08152-106">ResourceGroupParameterSet</span></span>
```
Get-AzAttestation [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08152-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08152-107">DESCRIPTION</span></span>
<span data-ttu-id="08152-108">Das Get-AzAttestation-Cmdlet erhält Informationen zur Bescheinigung in einem Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08152-108">The Get-AzAttestation cmdlet gets information about the attestation in a subscription.</span></span>

## <span data-ttu-id="08152-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08152-109">EXAMPLES</span></span>

### <span data-ttu-id="08152-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08152-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAttestation -Name example -ResourceGroupName rg1 
Id                  : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/rg1/providers/Microsoft.Attestation/attestationProviders/example
Name                : example
Type                : Microsoft.Attestation/attestationProviders
Status              : Ready
AttesUri            : https://example.us.attest.azure.net
ResoureGroupName    : rg1 
SubscriptionId      : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
```
<span data-ttu-id="08152-111">Besorgen Sie sich die Bescheinigung "Beispiel" in der Ressourcengruppe "RG1".</span><span class="sxs-lookup"><span data-stu-id="08152-111">Get Attestation "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="08152-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="08152-112">PARAMETERS</span></span>

### <span data-ttu-id="08152-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08152-113">-DefaultProfile</span></span>
<span data-ttu-id="08152-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08152-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08152-115">-Name</span><span class="sxs-lookup"><span data-stu-id="08152-115">-Name</span></span>
<span data-ttu-id="08152-116">Name der Bescheinigung.</span><span class="sxs-lookup"><span data-stu-id="08152-116">Attestation Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08152-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08152-117">-ResourceGroupName</span></span>
<span data-ttu-id="08152-118">Gibt den Namen der Ressourcengruppe an, die der abgefragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08152-118">Specifies the name of the resource group associated with the attestation being queried.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08152-119">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="08152-119">-ResourceId</span></span>
<span data-ttu-id="08152-120">Gibt den Namen der Resourcen-Nr. an, die der Befragten Bescheinigung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="08152-120">Specifies the name of the ResourceID associated with the attestation being queried</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08152-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08152-121">CommonParameters</span></span>
<span data-ttu-id="08152-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08152-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08152-123">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08152-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08152-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08152-124">INPUTS</span></span>

### <span data-ttu-id="08152-125">System. String</span><span class="sxs-lookup"><span data-stu-id="08152-125">System.String</span></span>

## <span data-ttu-id="08152-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08152-126">OUTPUTS</span></span>

### <span data-ttu-id="08152-127">Microsoft. Azure. Commands. Testat. Models. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="08152-127">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="08152-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="08152-128">NOTES</span></span>

## <span data-ttu-id="08152-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08152-129">RELATED LINKS</span></span>
