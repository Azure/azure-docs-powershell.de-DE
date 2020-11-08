---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179575"
---
# <span data-ttu-id="07025-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="07025-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="07025-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="07025-102">SYNOPSIS</span></span>
<span data-ttu-id="07025-103">Ruft den Protokollwiedergabe Dienststatus ab.</span><span class="sxs-lookup"><span data-stu-id="07025-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="07025-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="07025-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07025-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07025-105">DESCRIPTION</span></span>
<span data-ttu-id="07025-106">Das Cmdlet " **Get-AzSqlInstanceDatabaseLogReplay** " Ruft den Status des Protokollwiedergabe Diensts für die angegebene Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="07025-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="07025-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07025-107">EXAMPLES</span></span>

### <span data-ttu-id="07025-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="07025-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="07025-109">Mit diesem Befehl wird der Protokollwiedergabe Dienststatus für die angegebene Datenbank abgerufen.</span><span class="sxs-lookup"><span data-stu-id="07025-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="07025-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07025-110">PARAMETERS</span></span>

### <span data-ttu-id="07025-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07025-111">-DefaultProfile</span></span>
<span data-ttu-id="07025-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="07025-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07025-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="07025-113">-InstanceName</span></span>
<span data-ttu-id="07025-114">Der Name der Instanz.</span><span class="sxs-lookup"><span data-stu-id="07025-114">The name of the instance.</span></span>

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

### <span data-ttu-id="07025-115">-Name</span><span class="sxs-lookup"><span data-stu-id="07025-115">-Name</span></span>
<span data-ttu-id="07025-116">Der Name der abzurufenden Instanzen Datenbank.</span><span class="sxs-lookup"><span data-stu-id="07025-116">The name of the instance database to retrieve.</span></span>

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

### <span data-ttu-id="07025-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07025-117">-ResourceGroupName</span></span>
<span data-ttu-id="07025-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="07025-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="07025-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07025-119">CommonParameters</span></span>
<span data-ttu-id="07025-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07025-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07025-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07025-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07025-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="07025-122">INPUTS</span></span>

### <span data-ttu-id="07025-123">System. String</span><span class="sxs-lookup"><span data-stu-id="07025-123">System.String</span></span>

## <span data-ttu-id="07025-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="07025-124">OUTPUTS</span></span>

### <span data-ttu-id="07025-125">Microsoft. Azure. Commands. SQL. ManagedDatabase. Model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="07025-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="07025-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="07025-126">NOTES</span></span>

## <span data-ttu-id="07025-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="07025-127">RELATED LINKS</span></span>
