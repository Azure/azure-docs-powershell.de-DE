---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 41923067729b50a77f8660a7f626ac464619aa41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93818972"
---
# <span data-ttu-id="e8764-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="e8764-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="e8764-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e8764-102">SYNOPSIS</span></span>
<span data-ttu-id="e8764-103">Ruft die protokollierten Kategorien und Zeit Körner ab.</span><span class="sxs-lookup"><span data-stu-id="e8764-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="e8764-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8764-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e8764-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8764-105">DESCRIPTION</span></span>
<span data-ttu-id="e8764-106">Das Cmdlet " **Get-AzDiagnosticSetting** " Ruft die Kategorien und Zeit Körner ab, die für eine Ressource protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="e8764-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="e8764-107">Eine Zeit Körnung ist das Aggregations Intervall einer Metrik.</span><span class="sxs-lookup"><span data-stu-id="e8764-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="e8764-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e8764-108">EXAMPLES</span></span>

### <span data-ttu-id="e8764-109">Beispiel 1: Abrufen des Status der Protokollierungskategorien und Zeit Körnungen</span><span class="sxs-lookup"><span data-stu-id="e8764-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="e8764-110">Dieser Befehl ruft die Kategorien und Zeit Körner ab, die für einen Azure Key Vault *mit einer/Subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/Providers/Microsoft.keyvault/KeyVaults/ContosoKeyVault.* -Klasse protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="e8764-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="e8764-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8764-111">PARAMETERS</span></span>

### <span data-ttu-id="e8764-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8764-112">-DefaultProfile</span></span>
<span data-ttu-id="e8764-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e8764-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8764-114">-Name</span><span class="sxs-lookup"><span data-stu-id="e8764-114">-Name</span></span>
<span data-ttu-id="e8764-115">Der Name der Diagnose Einstellung.</span><span class="sxs-lookup"><span data-stu-id="e8764-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="e8764-116">Wenn der Anruf standardmäßig auf "Dienst" zurückgesetzt wird, wie es in der vorherigen API der Fall war.</span><span class="sxs-lookup"><span data-stu-id="e8764-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="e8764-117">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e8764-117">-ResourceId</span></span>
<span data-ttu-id="e8764-118">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="e8764-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="e8764-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8764-119">CommonParameters</span></span>
<span data-ttu-id="e8764-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8764-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8764-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8764-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8764-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e8764-122">INPUTS</span></span>

### <span data-ttu-id="e8764-123">System. String</span><span class="sxs-lookup"><span data-stu-id="e8764-123">System.String</span></span>

## <span data-ttu-id="e8764-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e8764-124">OUTPUTS</span></span>

### <span data-ttu-id="e8764-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="e8764-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="e8764-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="e8764-126">NOTES</span></span>

## <span data-ttu-id="e8764-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e8764-127">RELATED LINKS</span></span>

<span data-ttu-id="e8764-128">[Satz-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="e8764-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
