---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: 9cfe797482485abccdce8e7094b3f5caadf554ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932648"
---
# <span data-ttu-id="6a111-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="6a111-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="6a111-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a111-102">SYNOPSIS</span></span>
<span data-ttu-id="6a111-103">Ruft die protokollierten Kategorien und Zeitkörner ab.</span><span class="sxs-lookup"><span data-stu-id="6a111-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="6a111-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6a111-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a111-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6a111-105">DESCRIPTION</span></span>
<span data-ttu-id="6a111-106">Das **Get-AzDiagnosticSetting-Cmdlet** ruft die Kategorien und Zeitkörner ab, die für eine Ressource protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="6a111-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="6a111-107">Eine Zeitkörnung ist das Aggregationsintervall einer Metrik.</span><span class="sxs-lookup"><span data-stu-id="6a111-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="6a111-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6a111-108">EXAMPLES</span></span>

### <span data-ttu-id="6a111-109">Beispiel 1: Anzeigen des Status der Protokollierungskategorien und Zeitkörner</span><span class="sxs-lookup"><span data-stu-id="6a111-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="6a111-110">Dieser Befehl ruft die Kategorien und Zeitkörner ab, die für einen Azure Key Vault mit einer *ResourceId* von /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="6a111-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="6a111-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6a111-111">PARAMETERS</span></span>

### <span data-ttu-id="6a111-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a111-112">-DefaultProfile</span></span>
<span data-ttu-id="6a111-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6a111-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a111-114">-Name</span><span class="sxs-lookup"><span data-stu-id="6a111-114">-Name</span></span>
<span data-ttu-id="6a111-115">Der Name der Diagnoseeinstellung.</span><span class="sxs-lookup"><span data-stu-id="6a111-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="6a111-116">Wenn der Aufruf nicht standardmäßig auf "Dienst" festgelegt wurde, wie in der vorherigen API.</span><span class="sxs-lookup"><span data-stu-id="6a111-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="6a111-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a111-117">-ResourceId</span></span>
<span data-ttu-id="6a111-118">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="6a111-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="6a111-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a111-119">CommonParameters</span></span>
<span data-ttu-id="6a111-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a111-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a111-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a111-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a111-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6a111-122">INPUTS</span></span>

### <span data-ttu-id="6a111-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6a111-123">System.String</span></span>

## <span data-ttu-id="6a111-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6a111-124">OUTPUTS</span></span>

### <span data-ttu-id="6a111-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="6a111-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="6a111-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6a111-126">NOTES</span></span>

## <span data-ttu-id="6a111-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6a111-127">RELATED LINKS</span></span>

<span data-ttu-id="6a111-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="6a111-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
