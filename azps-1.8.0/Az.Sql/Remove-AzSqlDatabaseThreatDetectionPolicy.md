---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FCCB768A-A034-44AF-B4B6-2AD3133B08EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: b0ca96910d763cfcf40530ad99872e1e0d50ca31
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659057"
---
# <span data-ttu-id="da601-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="da601-101">Remove-AzSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="da601-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da601-102">SYNOPSIS</span></span>
<span data-ttu-id="da601-103">Entfernt die Bedrohungs Erkennungsrichtlinie aus einer Datenbank.</span><span class="sxs-lookup"><span data-stu-id="da601-103">Removes the threat detection policy from a database.</span></span>

## <span data-ttu-id="da601-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da601-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseThreatDetectionPolicy [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da601-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da601-105">DESCRIPTION</span></span>
<span data-ttu-id="da601-106">Das Cmdlet **Remove-AzSqlDatabaseThreatDetectionPolicy** entfernt die Bedrohungs Erkennungsrichtlinie aus einer AzureAzure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="da601-106">The **Remove-AzSqlDatabaseThreatDetectionPolicy** cmdlet removes the threat detection policy from an AzureAzure SQL database.</span></span>
<span data-ttu-id="da601-107">Um dieses Cmdlet zu verwenden, geben Sie die *ResourceGroupName* -und *Servername* -Parameter an, um die Datenbank zu identifizieren, aus der dieses Cmdlet die Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="da601-107">To use this cmdlet, specify the *ResourceGroupName* and *ServerName* parameters to identify the database from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="da601-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da601-108">EXAMPLES</span></span>

### <span data-ttu-id="da601-109">Beispiel 1: Entfernen einer Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="da601-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\>Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="da601-110">Dieser Befehl entfernt die Richtlinie für die Bedrohungserkennung aus einer Datenbank mit dem Namen Database01 auf dem Server mit dem Namen Server01.</span><span class="sxs-lookup"><span data-stu-id="da601-110">This command removes the threat detection policy from a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="da601-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="da601-111">PARAMETERS</span></span>

### <span data-ttu-id="da601-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="da601-112">-DatabaseName</span></span>
<span data-ttu-id="da601-113">Gibt den Namen einer Datenbank an, in der die Bedrohungs Erkennungsrichtlinie entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="da601-113">Specifies the name of a database where the threat detection policy should be removed.</span></span>

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

### <span data-ttu-id="da601-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da601-114">-DefaultProfile</span></span>
<span data-ttu-id="da601-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="da601-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da601-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="da601-116">-PassThru</span></span>
<span data-ttu-id="da601-117">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="da601-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="da601-118">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="da601-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="da601-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da601-119">-ResourceGroupName</span></span>
<span data-ttu-id="da601-120">Gibt den Namen der Ressourcengruppe an, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="da601-120">Specifies the name of the resource group the server belongs.</span></span>

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

### <span data-ttu-id="da601-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="da601-121">-ServerName</span></span>
<span data-ttu-id="da601-122">Gibt den Namen eines Servers an, auf dem die Datenbank ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da601-122">Specifies the name of a server on which the database runs.</span></span>

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

### <span data-ttu-id="da601-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da601-123">-Confirm</span></span>
<span data-ttu-id="da601-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da601-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da601-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da601-125">-WhatIf</span></span>
<span data-ttu-id="da601-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da601-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="da601-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da601-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da601-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da601-128">CommonParameters</span></span>
<span data-ttu-id="da601-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da601-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da601-130">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="da601-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da601-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da601-131">INPUTS</span></span>

### <span data-ttu-id="da601-132">System. String</span><span class="sxs-lookup"><span data-stu-id="da601-132">System.String</span></span>

## <span data-ttu-id="da601-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da601-133">OUTPUTS</span></span>

### <span data-ttu-id="da601-134">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="da601-134">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="da601-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="da601-135">NOTES</span></span>

## <span data-ttu-id="da601-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da601-136">RELATED LINKS</span></span>

[<span data-ttu-id="da601-137">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="da601-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


