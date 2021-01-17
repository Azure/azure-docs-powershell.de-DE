---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468472"
---
# <span data-ttu-id="6e1d7-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="6e1d7-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="6e1d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e1d7-102">SYNOPSIS</span></span>
<span data-ttu-id="6e1d7-103">Ruft den Dienststatus der Protokollwiedergabe ab.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="6e1d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6e1d7-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e1d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6e1d7-105">DESCRIPTION</span></span>
<span data-ttu-id="6e1d7-106">Das **Cmdlet "Get-AzSqlInstanceDatabaseLogReplay"** ruft den Dienststatus "Protokollwiedergabe" in der angegebenen Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="6e1d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6e1d7-107">EXAMPLES</span></span>

### <span data-ttu-id="6e1d7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6e1d7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="6e1d7-109">Mit diesem Befehl wird der Dienststatus für die Protokollwiedergabe in der angegebenen Datenbank angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="6e1d7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e1d7-110">PARAMETERS</span></span>

### <span data-ttu-id="6e1d7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e1d7-111">-DefaultProfile</span></span>
<span data-ttu-id="6e1d7-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e1d7-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6e1d7-113">-InstanceName</span></span>
<span data-ttu-id="6e1d7-114">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1d7-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6e1d7-115">-Name</span></span>
<span data-ttu-id="6e1d7-116">Der Name der abzurufende Instanzdatenbank.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1d7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e1d7-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e1d7-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e1d7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e1d7-119">CommonParameters</span></span>
<span data-ttu-id="6e1d7-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e1d7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e1d7-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e1d7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e1d7-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6e1d7-122">INPUTS</span></span>

### <span data-ttu-id="6e1d7-123">System.String</span><span class="sxs-lookup"><span data-stu-id="6e1d7-123">System.String</span></span>

## <span data-ttu-id="6e1d7-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6e1d7-124">OUTPUTS</span></span>

### <span data-ttu-id="6e1d7-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="6e1d7-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="6e1d7-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6e1d7-126">NOTES</span></span>

## <span data-ttu-id="6e1d7-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6e1d7-127">RELATED LINKS</span></span>
