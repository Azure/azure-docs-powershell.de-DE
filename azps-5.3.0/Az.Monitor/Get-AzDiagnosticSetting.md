---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 60B497F6-98A2-4C60-B142-FF5CD123362D
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDiagnosticSetting.md
ms.openlocfilehash: d1a6859638bfbcb69e479f4bc18a6a36c8aa68fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98470402"
---
# <span data-ttu-id="39bb8-101">Get-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="39bb8-101">Get-AzDiagnosticSetting</span></span>

## <span data-ttu-id="39bb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39bb8-102">SYNOPSIS</span></span>
<span data-ttu-id="39bb8-103">Ruft die protokollierten Kategorien und Zeitkörner ab.</span><span class="sxs-lookup"><span data-stu-id="39bb8-103">Gets the logged categories and time grains.</span></span>

## <span data-ttu-id="39bb8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="39bb8-104">SYNTAX</span></span>

```
Get-AzDiagnosticSetting [-ResourceId] <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39bb8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="39bb8-105">DESCRIPTION</span></span>
<span data-ttu-id="39bb8-106">Das **Cmdlet "Get-AzDiagnosticSetting"** ruft die Kategorien und Zeitkörner ab, die für eine Ressource protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="39bb8-106">The **Get-AzDiagnosticSetting** cmdlet gets the categories and time grains that are logged for a resource.</span></span>
<span data-ttu-id="39bb8-107">Ein Zeitmask ist das Aggregationsintervall einer Metrik.</span><span class="sxs-lookup"><span data-stu-id="39bb8-107">A time grain is the aggregation interval of a metric.</span></span>

## <span data-ttu-id="39bb8-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="39bb8-108">EXAMPLES</span></span>

### <span data-ttu-id="39bb8-109">Beispiel 1: Den Status der Protokollierungskategorien und Zeitkörner</span><span class="sxs-lookup"><span data-stu-id="39bb8-109">Example 1: Get the status of the logging categories and time grains</span></span>
```
PS C:\>Get-AzDiagnosticSetting -ResourceId "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault"
StorageAccountId   : /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.storage/accounts/ContosoStorageAccount
StorageAccountName : ContosoStorageAccount001
Metrics

Logs
Enabled  : True
Category : AuditEvent
```

<span data-ttu-id="39bb8-110">Dieser Befehl ruft die Kategorien und Zeitkörner ab, die für einen Azure Key Vault mit der *ResourceId* "/subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault" protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="39bb8-110">This command gets the categories and time grains that are logged for an Azure Key Vault with a *ResourceId* of /subscriptions/1a66ce04-b633-4a0b-b2bc-a912ec8986a6/ResourceGroups/ContosoRG/providers/microsoft.keyvault/KeyVaults/ContosoKeyVault.</span></span>

## <span data-ttu-id="39bb8-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39bb8-111">PARAMETERS</span></span>

### <span data-ttu-id="39bb8-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39bb8-112">-DefaultProfile</span></span>
<span data-ttu-id="39bb8-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="39bb8-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39bb8-114">-Name</span><span class="sxs-lookup"><span data-stu-id="39bb8-114">-Name</span></span>
<span data-ttu-id="39bb8-115">Der Name der Diagnoseeinstellung.</span><span class="sxs-lookup"><span data-stu-id="39bb8-115">The name of the diagnostic setting.</span></span> <span data-ttu-id="39bb8-116">Wird der Aufruf nicht standardmäßig auf "Service" festgelegt, wie in der vorherigen API.</span><span class="sxs-lookup"><span data-stu-id="39bb8-116">If not given the call default to "service" as it was in the previous API.</span></span>

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

### <span data-ttu-id="39bb8-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39bb8-117">-ResourceId</span></span>
<span data-ttu-id="39bb8-118">Gibt die ID der Ressource an.</span><span class="sxs-lookup"><span data-stu-id="39bb8-118">Specifies the ID of the resource.</span></span>

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

### <span data-ttu-id="39bb8-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39bb8-119">CommonParameters</span></span>
<span data-ttu-id="39bb8-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39bb8-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39bb8-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39bb8-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39bb8-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="39bb8-122">INPUTS</span></span>

### <span data-ttu-id="39bb8-123">System.String</span><span class="sxs-lookup"><span data-stu-id="39bb8-123">System.String</span></span>

## <span data-ttu-id="39bb8-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="39bb8-124">OUTPUTS</span></span>

### <span data-ttu-id="39bb8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="39bb8-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSServiceDiagnosticSettings</span></span>

## <span data-ttu-id="39bb8-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="39bb8-126">NOTES</span></span>

## <span data-ttu-id="39bb8-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="39bb8-127">RELATED LINKS</span></span>

<span data-ttu-id="39bb8-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md) 
 [Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="39bb8-128">[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)
[Remove-AzDiagnosticSetting](./Remove-AzDiagnosticSetting.md)</span></span>
