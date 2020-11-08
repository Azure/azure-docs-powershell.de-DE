---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: d4d2ae2ae8b09f319efe2f77030c88338b4c40b9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004513"
---
# <span data-ttu-id="732d6-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="732d6-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="732d6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="732d6-102">SYNOPSIS</span></span>
<span data-ttu-id="732d6-103">Ruft die erweiterte Bedrohungsschutz Richtlinie für ein Speicher-cosmosDB-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="732d6-103">Gets the advanced threat protection policy for a storage / cosmosDB account.</span></span>

## <span data-ttu-id="732d6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="732d6-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="732d6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="732d6-105">DESCRIPTION</span></span>
<span data-ttu-id="732d6-106">Das `Get-AzSecurityAdvancedThreatProtection` Cmdlet ruft die Richtlinie für den Bedrohungsschutz für ein Speicher-cosmosDB-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="732d6-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage / cosmosDB account.</span></span>
<span data-ttu-id="732d6-107">Um dieses Cmdlet zu verwenden, geben Sie den Parameter *resourcecode* an.</span><span class="sxs-lookup"><span data-stu-id="732d6-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="732d6-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="732d6-108">EXAMPLES</span></span>

### <span data-ttu-id="732d6-109">Beispiel 1: Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="732d6-109">Example 1 : Storage Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="732d6-110">Dieser Befehl ruft die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID ab `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="732d6-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

### <span data-ttu-id="732d6-111">Beispiel 2: CosmosDB-Konto</span><span class="sxs-lookup"><span data-stu-id="732d6-111">Example 2 : CosmosDB Account</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"

IsEnabled Id
--------- --
    True  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"
```
<span data-ttu-id="732d6-112">Dieser Befehl ruft die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID ab ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="732d6-112">This command gets the advanced threat protection policy for resource id ` "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.DocumentDb/databaseAccounts/myCosmosDBAccount/"`.</span></span>


## <span data-ttu-id="732d6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="732d6-113">PARAMETERS</span></span>

### <span data-ttu-id="732d6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="732d6-114">-DefaultProfile</span></span>
<span data-ttu-id="732d6-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="732d6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="732d6-116">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="732d6-116">-ResourceId</span></span>
<span data-ttu-id="732d6-117">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="732d6-117">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="732d6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="732d6-118">CommonParameters</span></span>
<span data-ttu-id="732d6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="732d6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="732d6-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="732d6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="732d6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="732d6-121">INPUTS</span></span>

### <span data-ttu-id="732d6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="732d6-122">System.String</span></span>

## <span data-ttu-id="732d6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="732d6-123">OUTPUTS</span></span>

### <span data-ttu-id="732d6-124">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="732d6-124">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="732d6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="732d6-125">NOTES</span></span>

## <span data-ttu-id="732d6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="732d6-126">RELATED LINKS</span></span>
