---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicymetadata
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyMetadata.md
ms.openlocfilehash: cfd32e7ee70ffb387bd1d2a52fdbf5eb60f2e148
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004678"
---
# <span data-ttu-id="06381-101">Get-AzPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="06381-101">Get-AzPolicyMetadata</span></span>

## <span data-ttu-id="06381-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06381-102">SYNOPSIS</span></span>
<span data-ttu-id="06381-103">Ruft Ressourcen für die Richtlinien Metadaten ab</span><span class="sxs-lookup"><span data-stu-id="06381-103">Gets Policy Metadata resources</span></span>

## <span data-ttu-id="06381-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06381-104">SYNTAX</span></span>

```
Get-AzPolicyMetadata [-Name <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06381-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06381-105">DESCRIPTION</span></span>
<span data-ttu-id="06381-106">Das Cmdlet " **Get-AzPolicyRemediation** " ruft alle Richtlinien Metadaten-Ressourcen oder eine bestimmte Richtlinien Metadaten-Ressource ab.</span><span class="sxs-lookup"><span data-stu-id="06381-106">The **Get-AzPolicyRemediation** cmdlet gets all policy metadata resources or a particular policy metadata resource.</span></span>

## <span data-ttu-id="06381-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06381-107">EXAMPLES</span></span>

### <span data-ttu-id="06381-108">Beispiel 1: Abrufen aller Ressourcen für die Richtlinien Metadaten</span><span class="sxs-lookup"><span data-stu-id="06381-108">Example 1: Get all policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata
```

<span data-ttu-id="06381-109">Dieser Befehl ruft alle Richtlinien Metadaten-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="06381-109">This command gets all policy metadata resources</span></span>

### <span data-ttu-id="06381-110">Beispiel 2: Abrufen einer Sammlung von 10 Richtlinien Metadaten-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="06381-110">Example 2: Get a collection of 10 policy metadata resources</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Top 10
```

<span data-ttu-id="06381-111">Dieser Befehl ruft eine Sammlung von 10 Richtlinien Metadaten-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="06381-111">This command gets a collection of 10 policy metadata resources</span></span>

### <span data-ttu-id="06381-112">Beispiel 3: Abrufen einer einzelnen Richtlinien Metadaten-Ressource mit dem Namen "ACF1348"</span><span class="sxs-lookup"><span data-stu-id="06381-112">Example 3: Get a single policy metadata resource with the name 'ACF1348'</span></span>
```powershell
PS C:\> Get-AzPolicyMetadata -Name ACF1348
```

<span data-ttu-id="06381-113">Dieser Befehl ruft eine einzelne Richtlinien Metadaten-Ressource mit dem Namen "ACF1348" ab.</span><span class="sxs-lookup"><span data-stu-id="06381-113">This command gets a single policy metadata resource with the name 'ACF1348'</span></span>

## <span data-ttu-id="06381-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="06381-114">PARAMETERS</span></span>

### <span data-ttu-id="06381-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06381-115">-DefaultProfile</span></span>
<span data-ttu-id="06381-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="06381-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06381-117">-Name</span><span class="sxs-lookup"><span data-stu-id="06381-117">-Name</span></span>
<span data-ttu-id="06381-118">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="06381-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06381-119">-Top</span><span class="sxs-lookup"><span data-stu-id="06381-119">-Top</span></span>
<span data-ttu-id="06381-120">Die maximale Anzahl der zurückzugebenden Richtlinien Metadaten-Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="06381-120">Maximum number of policy metadata resources to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06381-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06381-121">CommonParameters</span></span>
<span data-ttu-id="06381-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06381-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06381-123">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06381-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06381-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06381-124">INPUTS</span></span>

### <span data-ttu-id="06381-125">System. String</span><span class="sxs-lookup"><span data-stu-id="06381-125">System.String</span></span>

## <span data-ttu-id="06381-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06381-126">OUTPUTS</span></span>

### <span data-ttu-id="06381-127">Microsoft. Azure. Commands. PolicyInsights. Models. PSPolicyMetadata</span><span class="sxs-lookup"><span data-stu-id="06381-127">Microsoft.Azure.Commands.PolicyInsights.Models.PSPolicyMetadata</span></span>

## <span data-ttu-id="06381-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="06381-128">NOTES</span></span>

## <span data-ttu-id="06381-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06381-129">RELATED LINKS</span></span>
