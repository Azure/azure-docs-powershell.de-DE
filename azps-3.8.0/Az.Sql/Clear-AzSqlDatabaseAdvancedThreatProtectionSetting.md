---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Clear-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 7bdfb6ef415cdf5f3cac173730770307701b50bd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003925"
---
# <span data-ttu-id="080fc-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="080fc-101">Clear-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="080fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="080fc-102">SYNOPSIS</span></span>
<span data-ttu-id="080fc-103">Entfernt die erweiterten Bedrohungsschutz Einstellungen aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="080fc-103">Removes the advanced threat protection settings from a database.</span></span>

## <span data-ttu-id="080fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="080fc-104">SYNTAX</span></span>

```
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="080fc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="080fc-105">DESCRIPTION</span></span>
<span data-ttu-id="080fc-106">Das Cmdlet " **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** " entfernt die erweiterten Bedrohungsschutz Einstellungen aus einer AzureAzure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="080fc-106">The **Clear-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet removes the advanced threat protection settings from an AzureAzure SQL database.</span></span>
<span data-ttu-id="080fc-107">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren, aus der dieses Cmdlet die Einstellungen entfernt.</span><span class="sxs-lookup"><span data-stu-id="080fc-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the settings.</span></span>

## <span data-ttu-id="080fc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="080fc-108">EXAMPLES</span></span>

### <span data-ttu-id="080fc-109">Beispiel 1: Entfernen einer erweiterten Bedrohungsschutz Einstellungen für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="080fc-109">Example 1: Remove a advanced threat protection settings for a database</span></span>
```
PS C:\>Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="080fc-110">Mit diesem Befehl werden die erweiterten Bedrohungsschutz Einstellungen aus einer Datenbank namens Database01 auf dem Server mit dem Namen Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="080fc-110">This command removes the advanced threat protection settings from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="080fc-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="080fc-111">PARAMETERS</span></span>

### <span data-ttu-id="080fc-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="080fc-112">-DatabaseName</span></span>
<span data-ttu-id="080fc-113">Gibt den Namen einer Datenbank an, in der die erweiterten Bedrohungsschutz Einstellungen entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="080fc-113">Specifies the name of a database where the advanced threat protection settings should be removed.</span></span>

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

### <span data-ttu-id="080fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="080fc-114">-DefaultProfile</span></span>
<span data-ttu-id="080fc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="080fc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="080fc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="080fc-116">-PassThru</span></span>
<span data-ttu-id="080fc-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="080fc-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="080fc-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="080fc-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="080fc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="080fc-119">-ResourceGroupName</span></span>
<span data-ttu-id="080fc-120">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="080fc-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="080fc-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="080fc-121">-ServerName</span></span>
<span data-ttu-id="080fc-122">Gibt den Namen eines Servers an, auf dem die Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="080fc-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="080fc-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="080fc-123">-Confirm</span></span>
<span data-ttu-id="080fc-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="080fc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="080fc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="080fc-125">-WhatIf</span></span>
<span data-ttu-id="080fc-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="080fc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="080fc-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="080fc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="080fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="080fc-128">CommonParameters</span></span>
<span data-ttu-id="080fc-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="080fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="080fc-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="080fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="080fc-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="080fc-131">INPUTS</span></span>

### <span data-ttu-id="080fc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="080fc-132">System.String</span></span>

## <span data-ttu-id="080fc-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="080fc-133">OUTPUTS</span></span>

### <span data-ttu-id="080fc-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="080fc-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="080fc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="080fc-135">NOTES</span></span>

## <span data-ttu-id="080fc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="080fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="080fc-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="080fc-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


