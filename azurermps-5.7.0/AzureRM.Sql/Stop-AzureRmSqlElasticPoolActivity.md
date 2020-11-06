---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 87744454627feaadc8c953e1ad4e50016f14879f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500362"
---
# <span data-ttu-id="79c56-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="79c56-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="79c56-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79c56-102">SYNOPSIS</span></span>
<span data-ttu-id="79c56-103">Bricht den asynchronen Aktualisierungsvorgang für einen elastischen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="79c56-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79c56-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79c56-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79c56-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79c56-105">DESCRIPTION</span></span>
<span data-ttu-id="79c56-106">Mit dem Cmdlet " **Stop-AzureRmSqlElasticPoolActivity** " wird der asynchrone Aktualisierungsvorgang in einem elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="79c56-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="79c56-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79c56-107">EXAMPLES</span></span>

### <span data-ttu-id="79c56-108">Beispiel 1: Abbrechen des asynchronen Aktualisierungsvorgangs in einem elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="79c56-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete : 
```

<span data-ttu-id="79c56-109">Mit diesem Befehl wird der asynchrone Aktualisierungsvorgang für den elastischen Pool abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="79c56-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="79c56-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="79c56-110">PARAMETERS</span></span>

### <span data-ttu-id="79c56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c56-111">-DefaultProfile</span></span>
<span data-ttu-id="79c56-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79c56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c56-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79c56-113">-ElasticPoolName</span></span>
<span data-ttu-id="79c56-114">Der Name des Azure SQL-elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="79c56-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c56-115">-Vorgangs-Nr</span><span class="sxs-lookup"><span data-stu-id="79c56-115">-OperationId</span></span>
<span data-ttu-id="79c56-116">Die ID des abzurufenden Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="79c56-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c56-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c56-117">-ResourceGroupName</span></span>
<span data-ttu-id="79c56-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79c56-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="79c56-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="79c56-119">-ServerName</span></span>
<span data-ttu-id="79c56-120">Der Name des Azure SQL Server, in dem sich der elastische Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="79c56-120">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c56-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79c56-121">-Confirm</span></span>
<span data-ttu-id="79c56-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79c56-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c56-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c56-123">-WhatIf</span></span>
<span data-ttu-id="79c56-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79c56-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c56-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79c56-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c56-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c56-126">CommonParameters</span></span>
<span data-ttu-id="79c56-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c56-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c56-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79c56-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c56-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79c56-129">INPUTS</span></span>

### <span data-ttu-id="79c56-130">Keine</span><span class="sxs-lookup"><span data-stu-id="79c56-130">None</span></span>

<span data-ttu-id="79c56-131">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="79c56-131">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="79c56-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79c56-132">OUTPUTS</span></span>

### <span data-ttu-id="79c56-133">System. Object</span><span class="sxs-lookup"><span data-stu-id="79c56-133">System.Object</span></span>

## <span data-ttu-id="79c56-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="79c56-134">NOTES</span></span>

## <span data-ttu-id="79c56-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79c56-135">RELATED LINKS</span></span>



