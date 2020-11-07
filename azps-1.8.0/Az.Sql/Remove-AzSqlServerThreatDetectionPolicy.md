---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DCAB75A1-B4EF-4C41-9D6B-A954B6DB0028
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 5b75c2058fb7a6ddf323ebeaa6aad6967dcb5b01
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659030"
---
# <span data-ttu-id="3635d-101">Remove-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="3635d-101">Remove-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="3635d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3635d-102">SYNOPSIS</span></span>
<span data-ttu-id="3635d-103">Entfernt die Bedrohungs Erkennungsrichtlinie von einem Server.</span><span class="sxs-lookup"><span data-stu-id="3635d-103">Removes the threat detection policy from a server.</span></span>

## <span data-ttu-id="3635d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3635d-104">SYNTAX</span></span>

```
Remove-AzSqlServerThreatDetectionPolicy [-PassThru] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3635d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3635d-105">DESCRIPTION</span></span>
<span data-ttu-id="3635d-106">Das Remove-AzSqlServerThreatDetectionPolicy-Cmdlet entfernt die Richtlinie für die Bedrohungserkennung aus einem Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3635d-106">The Remove-AzSqlServerThreatDetectionPolicy cmdlet removes the threat detection policy from an Azure SQL server.</span></span>
<span data-ttu-id="3635d-107">Um dieses Cmdlet zu verwenden, geben Sie die ResourceGroupName-und Servername-Parameter an, um den Server zu identifizieren, auf dem dieses Cmdlet die Richtlinie entfernt.</span><span class="sxs-lookup"><span data-stu-id="3635d-107">To use this cmdlet, specify the ResourceGroupName and ServerName parameters to identify the server from which this cmdlet removes the policy.</span></span>

## <span data-ttu-id="3635d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3635d-108">EXAMPLES</span></span>

### <span data-ttu-id="3635d-109">Beispiel 1: Entfernen einer Bedrohungs Erkennungsrichtlinie für eine Datenbank</span><span class="sxs-lookup"><span data-stu-id="3635d-109">Example 1: Remove a threat detection policy for a database</span></span>
```
PS C:\> Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

<span data-ttu-id="3635d-110">Mit diesem Befehl wird die Bedrohungs Erkennungsrichtlinie von einem Server namens "Server01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="3635d-110">This command removes the threat detection policy from a server named Server01.</span></span>

## <span data-ttu-id="3635d-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="3635d-111">PARAMETERS</span></span>

### <span data-ttu-id="3635d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3635d-112">-DefaultProfile</span></span>
<span data-ttu-id="3635d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3635d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3635d-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3635d-114">-PassThru</span></span>
<span data-ttu-id="3635d-115">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3635d-115">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3635d-116">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3635d-116">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3635d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3635d-117">-ResourceGroupName</span></span>
<span data-ttu-id="3635d-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3635d-118">Specifies the name of the resource group the server is assigned to.</span></span>

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

### <span data-ttu-id="3635d-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="3635d-119">-ServerName</span></span>
<span data-ttu-id="3635d-120">Gibt den Namen eines Servers an.</span><span class="sxs-lookup"><span data-stu-id="3635d-120">Specifies the name of a server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3635d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3635d-121">-Confirm</span></span>
<span data-ttu-id="3635d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3635d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3635d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3635d-123">-WhatIf</span></span>
<span data-ttu-id="3635d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3635d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3635d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3635d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3635d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3635d-126">CommonParameters</span></span>
<span data-ttu-id="3635d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3635d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3635d-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3635d-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3635d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3635d-129">INPUTS</span></span>

### <span data-ttu-id="3635d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3635d-130">System.String</span></span>

## <span data-ttu-id="3635d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3635d-131">OUTPUTS</span></span>

### <span data-ttu-id="3635d-132">Microsoft. Azure. Commands. SQL. ThreatDetection. Model. ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="3635d-132">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="3635d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3635d-133">NOTES</span></span>

## <span data-ttu-id="3635d-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3635d-134">RELATED LINKS</span></span>

[<span data-ttu-id="3635d-135">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="3635d-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

