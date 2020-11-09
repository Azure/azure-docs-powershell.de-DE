---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300316"
---
# <span data-ttu-id="715f0-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="715f0-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="715f0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="715f0-102">SYNOPSIS</span></span>
<span data-ttu-id="715f0-103">Abrufen oder Auflisten eines verknüpften speicherkontos</span><span class="sxs-lookup"><span data-stu-id="715f0-103">Get or list linked storage account</span></span>

## <span data-ttu-id="715f0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="715f0-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="715f0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="715f0-105">DESCRIPTION</span></span>
<span data-ttu-id="715f0-106">Abrufen eines verknüpften speicherkontos, Auflisten aller verknüpften Speicherkonten, wenn "-DataSourceType" nicht angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="715f0-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="715f0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="715f0-107">EXAMPLES</span></span>

### <span data-ttu-id="715f0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="715f0-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="715f0-109">Listen verknüpfter Speicher Accoounts für Arbeitsbereich {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="715f0-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="715f0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="715f0-110">PARAMETERS</span></span>

### <span data-ttu-id="715f0-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="715f0-111">-DataSourceType</span></span>
<span data-ttu-id="715f0-112">Der Datenquellentyp sollte "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="715f0-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="715f0-113">-DefaultProfile</span></span>
<span data-ttu-id="715f0-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="715f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="715f0-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="715f0-115">-ResourceGroupName</span></span>
<span data-ttu-id="715f0-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="715f0-116">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f0-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="715f0-117">-WorkspaceName</span></span>
<span data-ttu-id="715f0-118">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="715f0-118">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715f0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715f0-119">CommonParameters</span></span>
<span data-ttu-id="715f0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715f0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715f0-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="715f0-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715f0-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="715f0-122">INPUTS</span></span>

### <span data-ttu-id="715f0-123">System. String</span><span class="sxs-lookup"><span data-stu-id="715f0-123">System.String</span></span>

## <span data-ttu-id="715f0-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="715f0-124">OUTPUTS</span></span>

### <span data-ttu-id="715f0-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="715f0-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="715f0-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="715f0-126">NOTES</span></span>

## <span data-ttu-id="715f0-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="715f0-127">RELATED LINKS</span></span>