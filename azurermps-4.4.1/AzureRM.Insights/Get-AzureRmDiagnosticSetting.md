---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 236ce405c222ba3b7746ba1affca8f288045f8a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663939"
---
# <span data-ttu-id="61cd9-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="61cd9-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="61cd9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61cd9-102">SYNOPSIS</span></span>
<span data-ttu-id="61cd9-103">Ruft die protokollierten Kategorien und Zeit Körner ab.</span><span class="sxs-lookup"><span data-stu-id="61cd9-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61cd9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61cd9-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61cd9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61cd9-105">DESCRIPTION</span></span>
<span data-ttu-id="61cd9-106">Das Cmdlet " **Get-AzureRmDiagnosticSetting** " Ruft die Kategorien und Zeit Körner ab, die für eine Ressource protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="61cd9-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="61cd9-107">Eine Zeit Körnung ist das Aggregations Intervall einer Metrik.</span><span class="sxs-lookup"><span data-stu-id="61cd9-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="61cd9-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61cd9-108">EXAMPLES</span></span>

### <span data-ttu-id="61cd9-109">Beispiel 1: Abrufen des Status der Protokollierungskategorien und Zeit Körnungen</span><span class="sxs-lookup"><span data-stu-id="61cd9-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="61cd9-110">Dieser Befehl ruft die Kategorien und Zeit Körner ab, die für einen Azure Key Vault *mit einer/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.* -Klasse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="61cd9-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="61cd9-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="61cd9-111">PARAMETERS</span></span>

### <span data-ttu-id="61cd9-112">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="61cd9-112">-ResourceId</span></span>
<span data-ttu-id="61cd9-113">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="61cd9-113">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="61cd9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61cd9-114">-DefaultProfile</span></span>
<span data-ttu-id="61cd9-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61cd9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61cd9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61cd9-116">CommonParameters</span></span>
<span data-ttu-id="61cd9-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61cd9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61cd9-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61cd9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61cd9-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61cd9-119">INPUTS</span></span>

## <span data-ttu-id="61cd9-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61cd9-120">OUTPUTS</span></span>

### <span data-ttu-id="61cd9-121">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="61cd9-121">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="61cd9-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="61cd9-122">NOTES</span></span>

## <span data-ttu-id="61cd9-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61cd9-123">RELATED LINKS</span></span>

[<span data-ttu-id="61cd9-124">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="61cd9-124">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


