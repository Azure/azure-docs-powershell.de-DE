---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174942"
---
# <span data-ttu-id="2c1cf-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2c1cf-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2c1cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c1cf-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1cf-103">Abrufen oder Auflisten eines verknüpften speicherkontos</span><span class="sxs-lookup"><span data-stu-id="2c1cf-103">Get or list linked storage account</span></span>

## <span data-ttu-id="2c1cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c1cf-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c1cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c1cf-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1cf-106">Abrufen eines verknüpften speicherkontos, Auflisten aller verknüpften Speicherkonten, wenn "-DataSourceType" nicht angegeben wurde</span><span class="sxs-lookup"><span data-stu-id="2c1cf-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="2c1cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c1cf-107">EXAMPLES</span></span>

### <span data-ttu-id="2c1cf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c1cf-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="2c1cf-109">Listen verknüpfter Speicher Accoounts für Arbeitsbereich {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="2c1cf-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="2c1cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c1cf-110">PARAMETERS</span></span>

### <span data-ttu-id="2c1cf-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2c1cf-111">-DataSourceType</span></span>
<span data-ttu-id="2c1cf-112">Der Datenquellentyp sollte "CustomLogs", "AzureWatson" sein.</span><span class="sxs-lookup"><span data-stu-id="2c1cf-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="2c1cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1cf-113">-DefaultProfile</span></span>
<span data-ttu-id="2c1cf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c1cf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1cf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c1cf-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c1cf-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c1cf-116">The resource group name.</span></span>

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

### <span data-ttu-id="2c1cf-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2c1cf-117">-WorkspaceName</span></span>
<span data-ttu-id="2c1cf-118">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="2c1cf-118">The workspace name.</span></span>

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

### <span data-ttu-id="2c1cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1cf-119">CommonParameters</span></span>
<span data-ttu-id="2c1cf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1cf-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2c1cf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1cf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c1cf-122">INPUTS</span></span>

### <span data-ttu-id="2c1cf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2c1cf-123">System.String</span></span>

## <span data-ttu-id="2c1cf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c1cf-124">OUTPUTS</span></span>

### <span data-ttu-id="2c1cf-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="2c1cf-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="2c1cf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c1cf-126">NOTES</span></span>

## <span data-ttu-id="2c1cf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c1cf-127">RELATED LINKS</span></span>