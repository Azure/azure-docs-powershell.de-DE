---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlSyncGroupSync.md
ms.openlocfilehash: e81667523327c9a83497ce4f586f166fe69d0dc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503166"
---
# <span data-ttu-id="9adfe-101">Start-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9adfe-101">Start-AzureRmSqlSyncGroupSync</span></span>

## <span data-ttu-id="9adfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9adfe-102">SYNOPSIS</span></span>
<span data-ttu-id="9adfe-103">Startet eine Synchronisierungsgruppen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="9adfe-103">Starts a sync group synchronization.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9adfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9adfe-104">SYNTAX</span></span>

```
Start-AzureRmSqlSyncGroupSync [-SyncGroupName] <String> [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9adfe-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9adfe-105">DESCRIPTION</span></span>
<span data-ttu-id="9adfe-106">Das Cmdlet **Start-AzureRmSqlSyncGroupSync** startet eine Synchronisierungsgruppen Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="9adfe-106">The **Start-AzureRmSqlSyncGroupSync** cmdlet starts a sync group synchronization.</span></span>

## <span data-ttu-id="9adfe-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9adfe-107">EXAMPLES</span></span>

### <span data-ttu-id="9adfe-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9adfe-108">Example 1</span></span>
```
PS C:\> Start-AzureRmSqlSyncGroupSync -SyncGroupName mysg [-ServerName] mysrv [-DatabaseName] mydb [-ResourceGroupName] myrg
```

<span data-ttu-id="9adfe-109">Mit diesem Befehl wird eine Synchronisierungs Runde für die Synchronisierungsgruppe mysg.</span><span class="sxs-lookup"><span data-stu-id="9adfe-109">This command starts a round of synchronization for the sync group mysg.</span></span>

## <span data-ttu-id="9adfe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9adfe-110">PARAMETERS</span></span>

### <span data-ttu-id="9adfe-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9adfe-111">-Confirm</span></span>
<span data-ttu-id="9adfe-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9adfe-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9adfe-113">-DatabaseName</span></span>
<span data-ttu-id="9adfe-114">Der Name der Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="9adfe-114">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9adfe-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9adfe-115">-PassThru</span></span>
<span data-ttu-id="9adfe-116">Definiert, ob die Synchronisierungsgruppe zurückgegeben wird</span><span class="sxs-lookup"><span data-stu-id="9adfe-116">Defines Whether return the sync group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9adfe-117">-ResourceGroupName</span></span>
<span data-ttu-id="9adfe-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9adfe-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="9adfe-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="9adfe-119">-ServerName</span></span>
<span data-ttu-id="9adfe-120">Der Name des Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9adfe-120">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-121">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9adfe-121">-SyncGroupName</span></span>
<span data-ttu-id="9adfe-122">Der Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9adfe-122">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9adfe-123">-WhatIf</span></span>
<span data-ttu-id="9adfe-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9adfe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9adfe-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9adfe-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9adfe-126">-DefaultProfile</span></span>
<span data-ttu-id="9adfe-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9adfe-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9adfe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9adfe-128">CommonParameters</span></span>
<span data-ttu-id="9adfe-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9adfe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9adfe-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9adfe-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9adfe-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9adfe-131">INPUTS</span></span>

## <span data-ttu-id="9adfe-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9adfe-132">OUTPUTS</span></span>

### <span data-ttu-id="9adfe-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="9adfe-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="9adfe-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="9adfe-134">NOTES</span></span>

## <span data-ttu-id="9adfe-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9adfe-135">RELATED LINKS</span></span>

[<span data-ttu-id="9adfe-136">Stopp-AzureRmSqlSyncGroupSync</span><span class="sxs-lookup"><span data-stu-id="9adfe-136">Stop-AzureRmSqlSyncGroupSync</span></span>](./Stop-AzureRmSqlSyncGroupSync.md)

