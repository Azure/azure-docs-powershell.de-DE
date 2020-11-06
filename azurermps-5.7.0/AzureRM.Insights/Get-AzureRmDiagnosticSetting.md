---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmDiagnosticSetting.md
ms.openlocfilehash: b5963aa588672bb2a8940d3f61f4cd67bef9c4a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476749"
---
# <span data-ttu-id="2ce27-101">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2ce27-101">Get-AzureRmDiagnosticSetting</span></span>

## <span data-ttu-id="2ce27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2ce27-102">SYNOPSIS</span></span>
<span data-ttu-id="2ce27-103">Ruft die protokollierten Kategorien und Zeit Körner ab.</span><span class="sxs-lookup"><span data-stu-id="2ce27-103">Gets the logged categories and time grains.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ce27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ce27-104">SYNTAX</span></span>

```
Get-AzureRmDiagnosticSetting [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ce27-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ce27-105">DESCRIPTION</span></span>
<span data-ttu-id="2ce27-106">Das Cmdlet " **Get-AzureRmDiagnosticSetting** " Ruft die Kategorien und Zeit Körner ab, die für eine Ressource protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="2ce27-106">The **Get-AzureRmDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>

<span data-ttu-id="2ce27-107">Eine Zeit Körnung ist das Aggregations Intervall einer Metrik.</span><span class="sxs-lookup"><span data-stu-id="2ce27-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="2ce27-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2ce27-108">EXAMPLES</span></span>

### <span data-ttu-id="2ce27-109">Beispiel 1: Abrufen des Status der Protokollierungskategorien und Zeit Körnungen</span><span class="sxs-lookup"><span data-stu-id="2ce27-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzureRmDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="2ce27-110">Dieser Befehl ruft die Kategorien und Zeit Körner ab, die für einen Azure Key Vault *mit einer/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.* -Klasse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="2ce27-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="2ce27-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ce27-111">PARAMETERS</span></span>

### <span data-ttu-id="2ce27-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ce27-112">-DefaultProfile</span></span>
<span data-ttu-id="2ce27-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2ce27-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ce27-114">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2ce27-114">-ResourceId</span></span>
<span data-ttu-id="2ce27-115">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="2ce27-115">Specifies the ID of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ce27-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ce27-116">CommonParameters</span></span>
<span data-ttu-id="2ce27-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ce27-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ce27-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ce27-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ce27-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2ce27-119">INPUTS</span></span>

### <span data-ttu-id="2ce27-120">Keine</span><span class="sxs-lookup"><span data-stu-id="2ce27-120">None</span></span>
<span data-ttu-id="2ce27-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2ce27-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2ce27-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2ce27-122">OUTPUTS</span></span>

### <span data-ttu-id="2ce27-123">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="2ce27-123">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="2ce27-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="2ce27-124">NOTES</span></span>

## <span data-ttu-id="2ce27-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2ce27-125">RELATED LINKS</span></span>

[<span data-ttu-id="2ce27-126">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="2ce27-126">Get-AzureRmDiagnosticSetting</span></span>](./Get-AzureRmDiagnosticSetting.md)


