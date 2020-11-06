---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlmanagedinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlInstance.md
ms.openlocfilehash: 1da1c431d41c7277a8291bb9a012218057b9c678
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501961"
---
# <span data-ttu-id="edac1-101">Remove-AzureRmSqlInstance</span><span class="sxs-lookup"><span data-stu-id="edac1-101">Remove-AzureRmSqlInstance</span></span>

## <span data-ttu-id="edac1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="edac1-102">SYNOPSIS</span></span>
<span data-ttu-id="edac1-103">Entfernt eine Azure SQL-Datenbankinstanz.</span><span class="sxs-lookup"><span data-stu-id="edac1-103">Removes an Azure SQL Managed Database Instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="edac1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="edac1-104">SYNTAX</span></span>

### <span data-ttu-id="edac1-105">RemoveInstanceFromInputParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="edac1-105">RemoveInstanceFromInputParameters (Default)</span></span>
```
Remove-AzureRmSqlInstance [-Name] <String> [-ResourceGroupName] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edac1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span><span class="sxs-lookup"><span data-stu-id="edac1-106">RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition</span></span>
```
Remove-AzureRmSqlInstance [-InputObject] <AzureSqlManagedInstanceModel> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="edac1-107">RemoveInstanceFromAzureResourceId</span><span class="sxs-lookup"><span data-stu-id="edac1-107">RemoveInstanceFromAzureResourceId</span></span>
```
Remove-AzureRmSqlInstance [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="edac1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="edac1-108">DESCRIPTION</span></span>
<span data-ttu-id="edac1-109">Das Cmdlet **Remove-AzureRmSqlInstance** entfernt eine Azure SQL-Daten Bank verwaltete Instanz.</span><span class="sxs-lookup"><span data-stu-id="edac1-109">The **Remove-AzureRmSqlInstance** cmdlet removes an Azure SQL Database Managed Instance.</span></span>

## <span data-ttu-id="edac1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="edac1-110">EXAMPLES</span></span>

### <span data-ttu-id="edac1-111">Beispiel 1: Entfernen einer Instanz</span><span class="sxs-lookup"><span data-stu-id="edac1-111">Example 1: Remove instance</span></span>
```
PS C:\>Remove-AzureRmSqlInstance -Name "managedInstance1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="edac1-112">Dieser Befehl entfernt die Instanz mit dem Namen managedInstance1.</span><span class="sxs-lookup"><span data-stu-id="edac1-112">This command removes the instance named managedInstance1.</span></span>

## <span data-ttu-id="edac1-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="edac1-113">PARAMETERS</span></span>

### <span data-ttu-id="edac1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edac1-114">-DefaultProfile</span></span>
<span data-ttu-id="edac1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="edac1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edac1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="edac1-116">-Force</span></span>
<span data-ttu-id="edac1-117">Bestätigungsmeldung zum Durchführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="edac1-117">Skip confirmation message for performing the action</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edac1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="edac1-118">-InputObject</span></span>
<span data-ttu-id="edac1-119">Das zu entfernende AzureSqlManagedInstanceModel-Objekt</span><span class="sxs-lookup"><span data-stu-id="edac1-119">The AzureSqlManagedInstanceModel object to remove</span></span>

```yaml
Type: AzureSqlManagedInstanceModel
Parameter Sets: RemoveInstanceFromAzureSqlManagedInstanceModelInstanceDefinition
Aliases: SqlInstance

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="edac1-120">-Name</span><span class="sxs-lookup"><span data-stu-id="edac1-120">-Name</span></span>
<span data-ttu-id="edac1-121">SQL-Instanzenname</span><span class="sxs-lookup"><span data-stu-id="edac1-121">SQL instance name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases: InstanceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edac1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edac1-122">-ResourceGroupName</span></span>
<span data-ttu-id="edac1-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="edac1-123">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromInputParameters
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edac1-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="edac1-124">-ResourceId</span></span>
<span data-ttu-id="edac1-125">Die Ressourcen-ID des zu entfernenden Instance-Objekts</span><span class="sxs-lookup"><span data-stu-id="edac1-125">The resource id of instance object to remove</span></span>

```yaml
Type: String
Parameter Sets: RemoveInstanceFromAzureResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edac1-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="edac1-126">-Confirm</span></span>
<span data-ttu-id="edac1-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="edac1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edac1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edac1-128">-WhatIf</span></span>
<span data-ttu-id="edac1-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="edac1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edac1-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="edac1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edac1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edac1-131">CommonParameters</span></span>
<span data-ttu-id="edac1-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edac1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edac1-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="edac1-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edac1-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="edac1-134">INPUTS</span></span>

### <span data-ttu-id="edac1-135">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="edac1-135">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="edac1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="edac1-136">System.String</span></span>

## <span data-ttu-id="edac1-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="edac1-137">OUTPUTS</span></span>

### <span data-ttu-id="edac1-138">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="edac1-138">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>

## <span data-ttu-id="edac1-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="edac1-139">NOTES</span></span>

## <span data-ttu-id="edac1-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="edac1-140">RELATED LINKS</span></span>
