---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 818B5302-91EE-425F-B1CD-86B626F1B7A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVault.md
ms.openlocfilehash: f667c0b13de510f7cf3e30e3faca9a93395ac221
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460900"
---
# <span data-ttu-id="28645-101">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="28645-101">Get-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="28645-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28645-102">SYNOPSIS</span></span>

<span data-ttu-id="28645-103">Ruft eine Liste der Wiederherstellungsdienste-Tresore ab.</span><span class="sxs-lookup"><span data-stu-id="28645-103">Gets a list of Recovery Services vaults.</span></span>

## <span data-ttu-id="28645-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="28645-104">SYNTAX</span></span>

### <span data-ttu-id="28645-105">ByTagNameValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="28645-105">ByTagNameValueParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] [-TagName <String>]
 [-TagValue <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28645-106">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="28645-106">ByTagObjectParameterSet</span></span>
```
Get-AzRecoveryServicesVault [[-ResourceGroupName] <String>] [[-Name] <String>] -Tag <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28645-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28645-107">DESCRIPTION</span></span>

<span data-ttu-id="28645-108">Das **Cmdlet "Get-AzRecoveryServicesVault"** ruft eine Liste der Recovery Services-Tresore im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="28645-108">The **Get-AzRecoveryServicesVault** cmdlet gets a list of Recovery Services vaults in the current subscription.</span></span>

## <span data-ttu-id="28645-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="28645-109">EXAMPLES</span></span>

### <span data-ttu-id="28645-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="28645-110">Example 1</span></span>

```
PS C:\> Get-AzRecoveryServicesVault
```

<span data-ttu-id="28645-111">Holen Sie sich die Liste des Tresors im ausgewählten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28645-111">Get the list of vault in selected subscription.</span></span>

### <span data-ttu-id="28645-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="28645-112">Example 2</span></span>

```
PS C:\> Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup"
```

<span data-ttu-id="28645-113">Holen Sie sich die Liste des Tresors in der Ressourcengruppe im ausgewählten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28645-113">Get the list of vault in resource group in selected subscription.</span></span>

### <span data-ttu-id="28645-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="28645-114">Example 3</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $vault.Identity | fl

PrincipalId : XXXXXXXX-XXXX-XXXX
TenantId    : XXXXXXXX-XXXX-XXXX
Type        : SystemAssigned
```

<span data-ttu-id="28645-115">Das erste Cmdlet ruft den Tresor in der Ressourcengruppe mit dem angegebenen Namen ab.</span><span class="sxs-lookup"><span data-stu-id="28645-115">The first cmdlet gets the vault in resource group with given name.</span></span> <span data-ttu-id="28645-116">Anschließend greifen wir auf die MSI-Informationen aus dem Tresor zu.</span><span class="sxs-lookup"><span data-stu-id="28645-116">Then we access the MSI information from the vault.</span></span>

## <span data-ttu-id="28645-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28645-117">PARAMETERS</span></span>

### <span data-ttu-id="28645-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28645-118">-DefaultProfile</span></span>

<span data-ttu-id="28645-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28645-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28645-120">-Name</span><span class="sxs-lookup"><span data-stu-id="28645-120">-Name</span></span>

<span data-ttu-id="28645-121">Gibt den Namen des Tresors an, nach dem eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28645-121">Specifies the name of the vault to query for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28645-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28645-122">-ResourceGroupName</span></span>

<span data-ttu-id="28645-123">Gibt den Namen der Azure-Ressourcengruppe an, aus der das angegebene Wiederherstellungsdienstobjekt abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="28645-123">Specifies the name of the Azure resource group from which to retrieve the specified Recovery Services object.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28645-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="28645-124">-Tag</span></span>

<span data-ttu-id="28645-125">Gibt die Tags an, die abgefragt werden müssen</span><span class="sxs-lookup"><span data-stu-id="28645-125">Specifies the Tags to query for</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28645-126">-TagName</span><span class="sxs-lookup"><span data-stu-id="28645-126">-TagName</span></span>

<span data-ttu-id="28645-127">Gibt den Schlüssel des tags an, für den eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28645-127">Specifies the Key of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28645-128">-TagValue</span><span class="sxs-lookup"><span data-stu-id="28645-128">-TagValue</span></span>

<span data-ttu-id="28645-129">Gibt den Wert des Tags an, für das eine Abfrage ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28645-129">Specifies the Value of the Tag to query for</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28645-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28645-130">CommonParameters</span></span>
<span data-ttu-id="28645-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28645-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28645-132">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28645-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28645-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="28645-133">INPUTS</span></span>

### <span data-ttu-id="28645-134">Keine</span><span class="sxs-lookup"><span data-stu-id="28645-134">None</span></span>

## <span data-ttu-id="28645-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="28645-135">OUTPUTS</span></span>

### <span data-ttu-id="28645-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="28645-136">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="28645-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="28645-137">NOTES</span></span>
<span data-ttu-id="28645-138">Get-AzRecoveryServicesVault in der alten Version von Az.RecoveryServices(<=2.10.0) kann mit Az.Accounts(>=1.8.1) aufgrund eines falschen Assemblyverweises nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="28645-138">Get-AzRecoveryServicesVault in old version of Az.RecoveryServices(<=2.10.0) cannot work with Az.Accounts(>=1.8.1) because of incorrect assembly reference.</span></span> <span data-ttu-id="28645-139">Das Modul Az.RecoveryServices muss auf 2.11.0 oder neuer aktualisiert werden, wenn Sie die neuesten Az- oder Az.-Konten verwenden.</span><span class="sxs-lookup"><span data-stu-id="28645-139">The module Az.RecoveryServices needs to be upgraded to 2.11.0 or newer if you are using the latest Az or Az.Accounts.</span></span>

## <span data-ttu-id="28645-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="28645-140">RELATED LINKS</span></span>

[<span data-ttu-id="28645-141">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="28645-141">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="28645-142">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="28645-142">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)

[<span data-ttu-id="28645-143">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="28645-143">Remove-AzRecoveryServicesVault</span></span>](./Remove-AzRecoveryServicesVault.md)
