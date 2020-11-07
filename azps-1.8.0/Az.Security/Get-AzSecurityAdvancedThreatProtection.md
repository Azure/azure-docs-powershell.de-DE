---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/get-azsecurityadvancedthreatprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdvancedThreatProtection.md
ms.openlocfilehash: 8957a794660750f45f295b77d921e647d368e7dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659464"
---
# <span data-ttu-id="9a7ab-101">Get-AzSecurityAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="9a7ab-101">Get-AzSecurityAdvancedThreatProtection</span></span>

## <span data-ttu-id="9a7ab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="9a7ab-103">Ruft die erweiterte Bedrohungsschutz Richtlinie für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-103">Gets the advanced threat protection policy for a storage account.</span></span>

## <span data-ttu-id="9a7ab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a7ab-104">SYNTAX</span></span>

```
Get-AzSecurityAdvancedThreatProtection -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a7ab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a7ab-105">DESCRIPTION</span></span>
<span data-ttu-id="9a7ab-106">Das `Get-AzSecurityAdvancedThreatProtection` Cmdlet ruft die Richtlinie für den Bedrohungsschutz für ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-106">The `Get-AzSecurityAdvancedThreatProtection` cmdlet gets the threat protection policy for a storage account.</span></span>
<span data-ttu-id="9a7ab-107">Um dieses Cmdlet zu verwenden, geben Sie den Parameter *resourcecode* an.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-107">To use this cmdlet, specify the *ResourceId* parameter.</span></span>

## <span data-ttu-id="9a7ab-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a7ab-108">EXAMPLES</span></span>

### <span data-ttu-id="9a7ab-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a7ab-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdvancedThreatProtection -ResourceId "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"

IsEnabled Id
--------- --
    False  "/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"
```

<span data-ttu-id="9a7ab-110">Dieser Befehl ruft die erweiterte Bedrohungsschutz Richtlinie für die Ressourcen-ID ab `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"` .</span><span class="sxs-lookup"><span data-stu-id="9a7ab-110">This command gets the advanced threat protection policy for resource id `"/subscriptions/xxxxxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myResourceGroup/providers/Microsoft.Storage/storageAccounts/myStorageAccount/"`.</span></span>

## <span data-ttu-id="9a7ab-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a7ab-111">PARAMETERS</span></span>

### <span data-ttu-id="9a7ab-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a7ab-112">-DefaultProfile</span></span>
<span data-ttu-id="9a7ab-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a7ab-114">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a7ab-114">-ResourceId</span></span>
<span data-ttu-id="9a7ab-115">Die ID der Sicherheitsressource, auf der Sie den Befehl aufrufen möchten.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-115">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9a7ab-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a7ab-116">CommonParameters</span></span>
<span data-ttu-id="9a7ab-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a7ab-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a7ab-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a7ab-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a7ab-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a7ab-119">INPUTS</span></span>

### <span data-ttu-id="9a7ab-120">System. String</span><span class="sxs-lookup"><span data-stu-id="9a7ab-120">System.String</span></span>

## <span data-ttu-id="9a7ab-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a7ab-121">OUTPUTS</span></span>

### <span data-ttu-id="9a7ab-122">Microsoft. Azure. Commands. Security. Models. AdvancedThreatProtection. PSAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="9a7ab-122">Microsoft.Azure.Commands.Security.Models.AdvancedThreatProtection.PSAdvancedThreatProtection</span></span>

## <span data-ttu-id="9a7ab-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a7ab-123">NOTES</span></span>

## <span data-ttu-id="9a7ab-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a7ab-124">RELATED LINKS</span></span>
